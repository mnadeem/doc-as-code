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

## Automatically

### Github Actions ⚙️

Using [GitHub Actions](https://github.com/features/actions) you can automate the deployment of your project documentation. At the root of your repository, create a new GitHub Actions workflow, e.g. `.github/workflows/ci.yml`, and copy and paste the following contents:  👇

```yaml
name: ci
on:
  push:
    branches:
      - master
jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: actions/setup-python@v2
        with:
          python-version: 3.x
      - run: pip install mkdocs-material
      - run: mkdocs gh-deploy --force
```

![](../img/deploying/github-actions.png)

### Jenkinsfile ⚙️

 If you have the following infrastructure

* Jenkins Instance
* Docker agent where mkdocs is installed.
* Jenkins pipleline infrastructure

Further do the following 👇

* Creating a Jenkins job (if you dont have organization plugin)
* Adding github webhook (if you dont have organization plugin)
* Adding Credentials to Jenkins instance
  
 Then Use the following jenkinsfile 👇

```pipeline
pipeline {
  agent { label 'docker-mkdocs-slave' }
  environment {
    ORG = 'Your ORG'  // This should be CHANGED
    REPO = 'Your Repo' // This should be CHANGED
    CREDENTIALS_ID = '{{JenkinsCredentialId}}'  // This should be CHANGED

    MKDOCS_VERSION = '1.0.4'
    LC_ALL='en_US.utf-8'
    LANG='en_US.utf-8'
  }
  stages {
    stage('Build & Deploy Docs') {
      when { branch 'master' }
      steps {
        withCredentials([usernamePassword(credentialsId: "$env.CREDENTIALS_ID", usernameVariable: 'USERNAME', passwordVariable: 'PASSWORD')]) {
          sh """
            . /etc/profile.d/jenkins.sh
            git config --global user.name "${USERNAME}"
            git remote set-url origin https://${USERNAME}:${PASSWORD}@github.com/${env.ORG}/${env.REPO}.git
            export GIT_USER=${USERNAME}:${PASSWORD}
            export GITHUB_HOST=github.com
            mkdocs gh-deploy --force
          """
        }
      }
    }
  }
}
```


### GitLab Pages ⚙️

If you're hosting your code on GitLab, deploying to [GitLab Pages](https://gitlab.com/pages) can be done by using the [GitLab CI](https://docs.gitlab.com/ee/ci/) task runner. At the root of your repository, create a task definition named `.gitlab-ci.yml` and copy and paste the following contents:  👇

```yaml
image: python:latest
pages:
  stage: deploy
  only:
    - master
  script:
    - pip install mkdocs-material
    - mkdocs build --site-dir public
  artifacts:
    paths:
      - public

```