# PACKAGE MANAGEMENT

## Add Package

```sh
uv add fastapi sqlalchemy redis
```

Uses `pyproject.toml` file to manage high-level dependencies. `uv.lock` lists all dependencies (including sub-dependencies) and their exact versions, so project is reproducible with same environment anywhere.

### Development Dependency

```sh
uv add --dev pytest
```

## Dependency Tree

```sh
uv tree
```

Shows dependency tree and versions installed.

## Synchronize

```sh
uv sync
```

Synchronize dependency and lock files.

## Remove

```sh
uv remove redis
```

Removes from dependency and lock files.
