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
