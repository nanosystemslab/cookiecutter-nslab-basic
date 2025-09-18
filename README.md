# cookiecutter-nslab-basic

A super-minimal [Cookiecutter](https://cookiecutter.readthedocs.io/) template for Python projects.  
It bootstraps a clean project with:

- 📦 [Poetry](https://python-poetry.org/) for dependency management
- 🧹 [Ruff](https://github.com/astral-sh/ruff) for linting & formatting
- 🔍 Optional [mypy](https://mypy-lang.org/) type checking
- ✅ [pytest](https://docs.pytest.org/) for testing
- 🔄 [pre-commit](https://pre-commit.com/) hooks

## Usage

Install Cookiecutter if you don't already have it:

```bash
pipx install cookiecutter
# or
pip install --user cookiecutter
```

Then generate a new project:

```bash
cookiecutter gh:nanosystemslab/cookiecutter-nslab-basic
```

You'll be prompted for:

- **project_name** → human-readable project name (also becomes the top-level directory)
- **package_name** → safe Python package name (defaults to slugified project name)
- **python_version** → target Python version (e.g. 3.11)
- **use_mypy** → whether to include mypy for type checking
- **license** → select from MIT, Apache-2.0, BSD-3-Clause, GPL-3.0-or-later, Proprietary

## Example

```bash
cookiecutter gh:nanosystemslab/cookiecutter-nslab-basic
```

Prompts:

```
project_name [My Awesome Project]: Can_Circularity_Analysis
package_name [can_circularity_analysis]:
python_version [3.11]:
use_mypy [n]: y
license [MIT]: GPL-3.0-or-later
```

Generated layout:

```
Can_Circularity_Analysis/
├── LICENSE
├── README.md
├── pyproject.toml
├── .pre-commit-config.yaml
├── src/
│   └── can_circularity_analysis/
│       └── __init__.py
└── tests/
    └── test_import.py
```

## Next steps inside the new project

```bash
cd Can_Circularity_Analysis
poetry install
poetry run pre-commit install
poetry run pre-commit run --all-files
poetry run pytest
```

## License

This template itself is licensed under the **MIT** license.
