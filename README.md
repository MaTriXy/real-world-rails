# Real World Rails

> Real World Rails applications and their open source codebases for developers to learn from

This is an actively maintained fork of [eliotsykes/real-world-rails](https://github.com/eliotsykes/real-world-rails), which was last updated in July 2024. Submodules are kept up to date and new notable Rails apps are added as they emerge.

This project brings 200+ active, open source Rails apps and engines together in one repository, making it easier for developers to download the collected codebases and learn from Rails apps written by experienced developers. Reading open source code can be an invaluable learning aid. You'll find the source code in the [`apps/`](apps/) and [`engines/`](engines/) subdirectories.

See [repos.md](repos.md) for the full list of included apps and engines with descriptions.

## How to install on your computer

Ensure you have git-lfs installed: https://git-lfs.com

```bash
# Clone this git repo:
git clone git@github.com:steveclarke/real-world-rails.git

cd real-world-rails/

# The Rails apps are linked to as git submodules.
GIT_LFS_SKIP_SMUDGE=1 git submodule update --init --single-branch --jobs 4
```

## How to update your local copy

Pull the latest commits from this repo and update submodules:
```bash
git pull
GIT_LFS_SKIP_SMUDGE=1 git submodule update
```

To update all submodules to the latest remote commits:
```bash
git submodule update --remote --jobs 8
```

## Other Real World Codebase Collections

- [Real World Ruby Apps](https://github.com/jeromedalbert/real-world-ruby-apps)
- [Real World Sinatra](https://github.com/jeromedalbert/real-world-sinatra)
- [Real World React](https://github.com/jeromedalbert/real-world-react)
- [Real World Django](https://github.com/ckrybus/real-world-django)

## Contributing

#### How to add a Real World Rails app

Given a GitHub repo for a Rails app `githubuser/foo`:

```bash
GIT_LFS_SKIP_SMUDGE=1 git submodule add -b <DEFAULT_BRANCH> git@github.com:githubuser/foo.git apps/foo
```

#### How to remove a submodule

Only use this if a previously public repo has been removed:

```bash
git submodule deinit -f path/to/submodule
rm -rf .git/modules/path/to/submodule
git rm -f path/to/submodule
```
