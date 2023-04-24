# PPC - Python Package Creator

Convenience tool for quickly creating new Python packages.

* Checks pypi.org for the availability of the project name.
* Creates repository on GitHub.
* Initializes repository with a Cookiecutter template.

## Installation

Before using the script, make sure to install the required dependencies:

```
pip install python-package-creator
```

## Usage

To use the PPC tool, you need to set the `GITHUB_TOKEN` environment variable with a valid GitHub token that has the necessary permissions for creating repositories.

```bash
export GITHUB_TOKEN=your_github_token
```

Now you can run the PPC command:

```
ppc <name> [--org organization]
```

<name>: The desired name for the Python package and GitHub repository.

[--org organization]: (Optional) The GitHub organization under which the repository will be created. If not provided, the repository will be created under your personal GitHub account.

## Example

Create a Python project with the name example_project:

```
poetry run ppc example_project
```

Create a Python project with the name example_project under the organization example_organization:

```
poetry run ppc example_project --org example_organization
```

## Configuration

The script reads the Cookiecutter template URL from a TOML configuration file. If the configuration file does not exist, it will be created with the default Cookiecutter URL: https://github.com/chrisdexler/cookiecutter-pypackage

You can change the default template by modifying the configuration file, located at the user config directory, with the file name my_cli.toml.
