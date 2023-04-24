# PPC - Python Project Creator

PPC is a command line tool for creating Python projects, checking package name availability on PyPI, initializing a GitHub repository, and pushing the project to the repository. It uses the Click package for the command line interface, the Requests package for making API calls, and the Cookiecutter package for generating project templates.

## Installation

Before using the script, make sure to install the required dependencies:

```
pip install poetry
```

Then, clone the repository and install the project's dependencies using Poetry:

```
git clone https://github.com/chrisdexler/ppc.git
cd ppc
poetry install
```

## Usage

To use the PPC tool, you need to set the `GITHUB_TOKEN` environment variable with a valid GitHub token that has the necessary permissions for creating repositories.

```bash
export GITHUB_TOKEN=your_github_token
```

Now you can run the PPC command:

```
poetry run ppc <name> [--org organization]
```

<name>: The desired name for the Python package and GitHub repository.

[--org organization]: (Optional) The GitHub organization under which the repository will be created. If not provided, the repository will be created under your personal GitHub account.
Example

Create a Python project with the name example_project:

<name>: The desired name for the Python package and GitHub repository.

[--org organization]: (Optional) The GitHub organization under which the repository will be created. If not provided, the repository will be created under your personal GitHub account.
Example

Create a Python project with the name example_project:

```
poetry run ppc example_project
```

Create a Python project with the name example_project under the organization example_organization:

```
poetry run ppc example_project --org example_organization
```

Configuration

The script reads the Cookiecutter template URL from a TOML configuration file. If the configuration file does not exist, it will be created with the default Cookiecutter URL: https://github.com/chrisdexler/cookiecutter-pypackage

You can change the default template by modifying the configuration file, located at the user config directory, with the file name my_cli.toml.
License

MIT License. See LICENSE for more information.
