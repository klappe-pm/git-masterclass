# Git Glossary

A reference for all key terms used throughout this course. Each term links back to the chapter where it is first introduced in context.

---

## B

**blob** — A Git object that stores raw file content. See [Chapter 16](./16-under-the-hood.md).

**branch** — A lightweight, movable pointer to a commit. See [Chapter 4](./04-working-with-branches.md).

---

## C

**cherry-pick** — Applying a specific commit from one branch onto another. See [Chapter 19](./19-reflog-bisect-cherry-pick.md).

**clone** — Downloading a full copy of a remote repository, including all history. See [Chapter 5](./05-introduction-to-github.md).

**commit** — A permanent snapshot of staged changes, stored in the repository. See [Chapter 3](./03-basic-git-commands.md).

**commit object** — The Git object that stores a tree pointer, parent reference, author, and message. See [Chapter 16](./16-under-the-hood.md).

**conflict** — When two branches modify the same part of the same file and Git cannot auto-merge. See [Chapter 10](./10-conflicts.md).

---

## D

**DAG (Directed Acyclic Graph)** — The data structure Git uses to store commit history. See [Chapter 16](./16-under-the-hood.md).

**detached HEAD** — A state where HEAD points to a commit hash instead of a branch. See [Chapter 4](./04-working-with-branches.md).

**distributed VCS** — A version control system where every developer has a full copy of the repository. See [Chapter 1](./01-introduction.md).

---

## F

**fast-forward merge** — A merge that simply moves a branch pointer forward because no divergent history exists. See [Chapter 9](./09-merging.md).

**fetch** — Downloading remote changes without merging them into your working branch. See [Chapter 6](./06-remote-repositories.md).

**fork** — A personal copy of someone else's repository, hosted on GitHub. See [Chapter 5](./05-introduction-to-github.md).

---

## H

**HEAD** — A special pointer indicating the currently checked-out commit or branch. See [Chapter 4](./04-working-with-branches.md).

**hook** — A script that Git runs automatically at specific points in the workflow. See [Chapter 21](./21-hooks-and-webhooks.md).

---

## I

**index** — Another name for the staging area. See [Chapter 3](./03-basic-git-commands.md).

---

## M

**merge** — Integrating changes from one branch into another. See [Chapter 9](./09-merging.md).

**merge commit** — A commit with two parent commits, created during a 3-way merge. See [Chapter 9](./09-merging.md).

**monorepo** — A single repository containing multiple related projects. See [Chapter 22](./22-submodules-subtrees-monorepos.md).

---

## O

**origin** — The conventional name for the primary remote repository. See [Chapter 6](./06-remote-repositories.md).

---

## P

**pull** — A combined fetch + merge (or fetch + rebase) operation. See [Chapter 6](./06-remote-repositories.md).

**pull request (PR)** — A GitHub feature for proposing and reviewing changes before merging. See [Chapter 15](./15-pull-requests.md).

**push** — Uploading local commits to a remote repository. See [Chapter 6](./06-remote-repositories.md).

---

## R

**rebase** — Replaying commits from one branch on top of another to produce a linear history. See [Chapter 11](./11-rebasing.md).

**reflog** — A local log of every movement of HEAD, used to recover lost commits. See [Chapter 19](./19-reflog-bisect-cherry-pick.md).

**remote** — A version of the repository hosted on a server. See [Chapter 6](./06-remote-repositories.md).

**repository (repo)** — A directory tracked by Git, containing project files and a `.git/` folder. See [Chapter 1](./01-introduction.md).

**revert** — Creating a new commit that undoes the changes of a previous commit. See [Chapter 14](./14-reverting-commits-and-tags.md).

---

## S

**SHA-1** — A 40-character hexadecimal hash used to uniquely identify every Git object. See [Chapter 16](./16-under-the-hood.md).

**squash** — Combining multiple commits into a single commit. See [Chapter 12](./12-squashing.md).

**staging area** — A preparation zone where changes are assembled before committing. See [Chapter 3](./03-basic-git-commands.md).

**stash** — Temporarily shelving uncommitted changes to allow context switching. See [Chapter 13](./13-stashing.md).

**submodule** — An embedded reference to another repository at a specific commit. See [Chapter 22](./22-submodules-subtrees-monorepos.md).

---

## T

**tag** — A permanent, named label on a specific commit, typically used for releases. See [Chapter 14](./14-reverting-commits-and-tags.md).

**tree object** — A Git object that maps filenames to blob hashes, representing a directory. See [Chapter 16](./16-under-the-hood.md).

**trunk-based development** — A workflow where all developers commit frequently to a single main branch. See [Chapter 18](./18-git-workflows.md).

---

## W

**webhook** — An HTTP callback GitHub fires when repository events occur. See [Chapter 21](./21-hooks-and-webhooks.md).

**working directory** — The local filesystem view of your project files. See [Chapter 3](./03-basic-git-commands.md).
