# forformat pre-commit mirror

This repository provides pre-commit hooks for
[forformat](https://github.com/cmbant/forformat).

It installs the published `forformat` package from PyPI, allowing pre-commit to use the
platform-specific wheels rather than building forformat from source.

Tags in this repository mirror published `forformat` versions: tag `vX.Y.Z` pins
`forformat==X.Y.Z`. A scheduled workflow checks PyPI, tests the hooks, updates the single dependency
pin, and creates the matching tag after a new release is installable.

## Usage

Use the latest release tag in your `.pre-commit-config.yaml`:

```yaml
repos:
  - repo: https://github.com/cmbant/forformat-pre-commit
    rev: vX.Y.Z
    hooks:
      - id: forformat
```

To check formatting without modifying files:

```yaml
repos:
  - repo: https://github.com/cmbant/forformat-pre-commit
    rev: vX.Y.Z
    hooks:
      - id: forformat-check
```

`pre-commit autoupdate` can update an existing configuration to the newest mirror tag.

See the main [forformat repository](https://github.com/cmbant/forformat) for documentation and
configuration.
