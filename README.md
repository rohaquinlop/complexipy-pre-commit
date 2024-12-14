# complexipy-pre-commit

A [pre-commit](https://pre-commit.com/) hook for [Complexipy](https://github.com/rohaquinlop/complexipy).

Distributed as a standalone repository to enable installing complexipy via prebuilt wheels from [PyPI](https://pypi.org/project/complexipy/).

### Using complexipy with pre-commit

To run Complexipy's [linter](https://github.com/rohaquinlop/complexipy) via pre-commit, add the following to your `.pre-commit-config.yaml`:

```yaml
repos:
- repo: https://github.com/illusional/complexipy-pre-commit
  # complexipy version.
  rev: v0.5.0
  hooks:
    # Run the cognitive complexity checker.
    - id: complexipy
```
To avoid running on Jupyter Notebooks, remove `jupyter` from the list of allowed filetypes:

```yaml
repos:
- repo: https://github.com/illusional/complexipy-pre-commit
  # complexipy version.
  rev: v0.5.0
  hooks:
    # Run the cognitive complexity checker.
    - id: complexipy
      types_or: [ python, pyi ]
```
