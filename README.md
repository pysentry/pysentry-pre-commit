# PySentry Pre-commit Hooks

Pre-commit hooks for [PySentry](https://github.com/nyudenkov/pysentry) security scanner.

## Pre-commit Integration

### Setup

Add PySentry to your `.pre-commit-config.yaml`:

```yaml
repos:
  - repo: https://github.com/pysentry/pysentry-pre-commit
    rev: v0.3.14
    hooks:
      - id: pysentry # default pysentry settings
```

### Advanced Configuration

```yaml
repos:
  - repo: https://github.com/pysentry/pysentry-pre-commit
    rev: v0.3.14
    hooks:
      - id: pysentry
        args: ["--sources", "pypa,osv", "--fail-on", "high"]
```
