pipeline {
  agent any
  stages {
    stage('Fetch') {
      steps {
        git(url: 'https://github.com/ansal-sajan/test-deploy.git', branch: 'master')
      }
    }

    stage('install webserver') {
      steps {
        sh 'sudo apt install apache2'
      }
    }

    stage('deploy') {
      steps {
        sh 'sudo cp -R index.html /var/www/html/'
      }
    }

  }
}