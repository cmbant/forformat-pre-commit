# forformat pre-commit mirror

This repository provides pre-commit hooks for
[forformat](https://github.com/cmbant/forformat).

It installs the published `forformat` package from PyPI, allowing
pre-commit to use the platform-specific wheels rather than building
forformat from source.

## Usage

```yaml
repos:
  - repo: https://github.com/cmbant/forformat-pre-commit
    rev: v0.1.4
    hooks:
      - id: forformat
```

To check formatting without modifying files:

```yaml
repos:
  - repo: https://github.com/cmbant/forformat-pre-commit
    rev: v0.1.4
    hooks:
      - id: forformat-check
```

See the main [forformat repository](https://github.com/cmbant/forformat)
for documentation and configuration.
