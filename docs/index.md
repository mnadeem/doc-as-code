# Welcome to MkDocs

For full documentation visit [mkdocs.org](https://www.mkdocs.org).

## Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.
* `mkdocs gh-deploy --force` - builds the docs and pushes the content to `gh-pages` branch, for more details refer [**this**](https://www.mkdocs.org/user-guide/deploying-your-docs/)


??? info "mkdocs gh-deploy"            
    
    ```
      E:\mkdocs\doc-as-code>mkdocs gh-deploy --force
      INFO    -  Cleaning site directory
      INFO    -  Building documentation to directory: E:\mkdocs\doc-as-code\site
      INFO    -  Documentation built in 1.44 seconds
      INFO    -  Copying 'E:\mkdocs\doc-as-code\site' to 'gh-pages' branch and pushing to GitHub.
      INFO    -  Your documentation should shortly be available at: https://mnadeem.github.io/doc-as-code/
    ```

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.
