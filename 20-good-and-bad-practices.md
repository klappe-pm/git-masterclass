# Chapter 20: Good and Bad Practices

Knowing the commands is one thing. Using them well is another. This chapter covers the conventions and habits that separate clean, professional repositories from chaotic ones.

## Commit Hygiene

### Write Meaningful Commit Messages

The **imperative mood** reads naturally in the context of "this commit will…":

```
# Good
feat: add email validation to registration form
fix: prevent double-submit on payment button
chore: update eslint to v8

# Bad
fixed stuff
WIP
asdfgh
updated files
```

Consider adopting **Conventional Commits** (`feat:`, `fix:`, `chore:`, `docs:`, `refactor:`, `test:`). It makes changelogs and semantic versioning automatable.

### Keep Commits Focused

Each commit should represent one logical change. A reviewer should be able to read the diff and understand exactly what changed and why.

```bash
# Stage individual hunks, not whole files
git add -p
```

If you find yourself writing "and" in a commit message, it probably should be two commits.

## Branch Hygiene

- Create a branch for every change — never commit directly to `main`
- Keep branches short-lived — merge within a few days, not weeks
- Delete branches after they are merged

```bash
# Clean up local branches that have been merged
git branch --merged main | grep -v "^\* main" | xargs git branch -d

# Clean up stale remote-tracking refs
git fetch --prune
```

## Secrets and Sensitive Data

**Never commit secrets to a repository** — not even a private one. This includes:

- API keys, tokens, passwords
- `.env` files containing credentials
- Private keys (`.pem`, `.key`)
- Database connection strings

Always add these to `.gitignore` **before** creating them. Use environment variables and secrets managers in CI/CD.

If you accidentally commit a secret:

1. **Immediately revoke the key** — assume it has been compromised
2. Remove it from history using `git filter-repo` (the modern replacement for `filter-branch`)
3. Force-push the rewritten history
4. Notify your team

```bash
# Remove a file from all history (install git-filter-repo first)
git filter-repo --path secrets.json --invert-paths
```

## Force Push Safely

`git push --force` overwrites the remote branch with your local version. Never use it on shared branches. If you must use it:

```bash
# Safer: only force-push if the remote hasn't changed since your last fetch
git push --force-with-lease
```

`--force-with-lease` refuses the push if someone else has pushed to the branch since you last fetched — preventing you from silently overwriting their work.

## The .gitignore Checklist

Before your first commit in any project, ensure your `.gitignore` covers:

```
# Language-specific build output and caches
node_modules/   dist/   __pycache__/   *.pyc   target/

# Environment and secrets
.env   .env.*   *.pem   *.key   secrets.*

# Editor metadata
.vscode/   .idea/   *.swp

# OS clutter
.DS_Store   Thumbs.db
```

Use **gitignore.io** to generate language-specific templates.

---

→ **Next:** [Chapter 21: Hooks and Webhooks](./21-hooks-and-webhooks.md)
← **Prev:** [Chapter 19: Reflog + Bisect + Cherry Pick](./19-reflog-bisect-cherry-pick.md)
