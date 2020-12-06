
# Document as Code

## Getting Started

### Prerequisites
In order to run your MkDocs page locally, you'll need Python installed on your machine, as well as the Python package manager, pip. You can check if you have these already installed from the command line:

```zsh
python --version
pip --version
```

Install the `mkdocs` package using pip, as well as other dependencies, such as the theme this template uses:

```zsh
pip install mkdocs mkdocs-material
```

### Development
To start working on your documentation locally, you will need to clone this repo:

```zsh
git clone https://github.com/mnadeem/doc-as-code.git
cd doc-as-code
```

To start up the server, run this command:

```zsh
mkdocs serve
```

Open http://127.0.0.1:8000 in a browser to see the documentation page you have created! 🎉 

## Project layout
Your repository will resemble the directory structure here: 

    mkdocs.yml    # The configuration file
    docs/
        index.md  # The documentation homepage
        img/      # Image directory
        ...       # Other directories with Markdown pages

## Deployment

Refer [**this**](deploying.md) for more details.

## Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.
* `mkdocs gh-deploy --force` - builds the docs and pushes the content to `gh-pages` branch, for more details refer [**this**](https://www.mkdocs.org/user-guide/deploying-your-docs/)
