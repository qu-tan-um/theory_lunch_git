# Theory Lunch on Git
Tutorial: [YouTube video](https://youtu.be/rH3zE7VlIMs?si=wRHP4x8sS3ga6OY3),
Reference: [ProGit book](https://git-scm.com/book/en/v2)

## Getting a repo, making a commit
- GitHub webpage + IDE extension (VS Code).
- Cloning a repository: GitHub CLI.
    - Or `git clone git@foo` when SSH is set up.
    - You can specify a directory name: `git clone git@foo <dir>`.
- GitHub Desktop just to avoid terminal?
- Stage your changes and commit. Then you always have these changes somewhere.
- Sync: fetch and push.
- Config (possible message): 
```
Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.
```

## Git internals
- Anything in Git is a file.
- Files can be accessed with Hash: `git cat-file -p foo`
- Directed acyclic graph of commits. In each commit:
    - Tree: root dir of repo, has further trees or blobs. 
    - Parent: hash of a commit
    - Metadata: author, commiter, message
- `.gitignore`

## Ah oh
```
> git pull --tags origin main
From https://github.com/qu-tan-um/theory_lunch_git
 * branch            main       -> FETCH_HEAD
hint: You have divergent branches and need to specify how to reconcile them.
hint: You can do so by running one of the following commands sometime before
hint: your next pull:
hint:
hint:   git config pull.rebase false  # merge
hint:   git config pull.rebase true   # rebase
hint:   git config pull.ff only       # fast-forward only
hint:
hint: You can replace "git config" with "git config --global" to set a default
hint: preference for all repositories. You can also pass --rebase, --no-rebase,
hint: or --ff-only on the command line to override the configured default per
hint: invocation.
fatal: Need to specify how to reconcile divergent branches.
```
- git pull: merge, rebase, fast-forward
- git reset --soft HEAD~1: keep all your changes while removing previous commit.
