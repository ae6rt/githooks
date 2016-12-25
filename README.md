## Git Hooks

Configure a global git hooks directory

```bash
$ git config --global core.hookspath ~/lib/githooks/
```

Make the hooks executable and place them in the hooks directory.

### prepare-commit-msg

Adds a default commit message of the form

```
[PROJ-666] <you must have a one-line banner-type message here>
```

The hook assumes you have feature branches with names that look like *feature/PROJ-666*.