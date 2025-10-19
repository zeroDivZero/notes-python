# `uvx`

Running Python tool without installing it globally.

E.g., to use `black` to fix formatting:

```sh
uvx black main.py
```

Creates in background temporary, isolated environment, installs tool, and executes. Cached for repeated performance.
