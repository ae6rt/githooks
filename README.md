# Git Hooks

Git hooks allow you to process git metadata at various points in the commit cycle.  Reference:  https://git-scm.com/docs/githooks

Configure a global git hooks directory

```bash
$ git config --global core.hookspath ~/lib/githooks/
```

Make the hooks executable and place them in the hooks directory.

## Client side hooks

### prepare-commit-msg

This hook assumes you have feature branches with names that look like *feature/PROJ-666*.

#### git commit \<return\>

Places you in the editor with a default commit message of the form

```
[PROJ-666] <you must have a one-line banner-type message here>
```

#### git commit -m "msg"

Creates a commit message of the form

```
[PROJ-666] msg
```

#### git commit -m "one" -m "two"

Creates a commit message of the form

```
[PROJ-666] one

two
```

