# Theory Lunch on Git
Tutorial: [YouTube video](https://youtu.be/rH3zE7VlIMs?si=wRHP4x8sS3ga6OY3),
Reference: [ProGit book](https://git-scm.com/book/en/v2)

## Getting a repo, making a commit
- GitHub webpage + IDE extension (VS Code).
- Cloning a repository: GitHub CLI.
    - Or `git clone git@foo` when SSH is set up.
    - You can specify a directory name: `git clone git@foo <dir>`.
- GitHub Desktop just to avoid terminal?
- Stage your changes and commit.
- Sync: fetch and push.
- Config: 
```
Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.
```

## Git internals
- Anything in Git is a file.
- Files can be accessed with Hash.
