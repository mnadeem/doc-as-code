---
title: Deploying Document As Code
description: Various options to deploy the markdown
authors:
    - Mohammad Nadeem
date: 2020-11-29
---

Markdown pages needs to be converted to HTML pages, and should be deployed to a place to be served.

Normally markdown is pushed to `main/master` branch 🔀 and in case of github, the static contents are automatically served rom `gh-pages` branch

## Manually

The following command would build the current branch and push the static site to `gh-pages` branch, if you are doing this for the first time, `gh-pages` brach might not exist in this case it would automatically create this branch for you.

```bash
mkdocs gh-deploy
```

??? abstract "Sample output"

    ```bash
    INFO    -  Cleaning site directory
    INFO    -  Building documentation to directory: E:\mkdocs\doc-as-code\site
    INFO    -  Documentation built in 1.66 seconds
    INFO    -  Copying 'E:\mkdocs\doc-as-code\site' to 'gh-pages' branch and pushing to GitHub.
    INFO    -  Your documentation should shortly be available at: https://mnadeem.github.io/doc-as-code/
    ```
