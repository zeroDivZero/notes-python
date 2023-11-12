# WHAT IS `pyenv`

[https://github.com/pyenv/pyenv]

Python environment management system to switch between versions of Python.

Can change global Python version per user, specify per-project version, and allows overriding version with environment variable. Can search for commands from multiple Python versions.

## How it Works

Pyenv intercepts Python commands using **shim** executables injected into `PATH`, determines which version specified by app, and passes commands to correct Python installation.

### Shims

Pyenv inserts directory of shims in `PATH`:

```sh
$(pyenv root)/shims:/usr/local/bin:/usr/bin:/bin
```

Through *rehashing* process, pyenv maintains shims in that directory to match every Python command across every installed Python version — `python`, `pip`, etc.

Shims are lightweight executables that pass commands to pyenv. E.g., when running `pip`, OS:

1. Searches `PATH` for `pip`.
2. Finds pyenv shim named `pip`.
3. Runs shim named `pip`, which in turn passes command to pyenv.

### Version Selection

When executing shim, pyenv determines Python version in this order:

1. `PYENV_VERSION` environment variable (if specified). Use `pyenv shell` to set it for current shell session.

2. App-specific `.python-version` file in current directory (if present). Modify with `pyenv local`.

3. First `.python-version` file found (if any) by searching each parent directory, until filesystem root.

4. Global `$(pyenv root)/version` file. Modify with `pyenv global` command.

If global not present, pyenv defaults to `system` Python, which is version found on `PATH` after shims entry (i.e., whatever would run if pyenv shims weren't on `PATH`). Not managed by pyenv.
