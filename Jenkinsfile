pipeline {
  agent any
  stages {
    stage('Git') {
      steps {
        git 'https://github.com/austinrain03/flask.git'
      }
    }

    stage('Build') {
      steps {
        sh 'docker build -t austinrain03/flask_app .'
      }
    }

    stage('Docker Login ') {
      steps {
        sh 'docker login -u austinrain03 -p dckr_pat_qWPZB6FeBKjMt2dLVf3iht-9Tvs'
      }
    }

    stage('Docker Push') {
      steps {
        sh 'docker push austinrain03/flask_app'
      }
    }

  }
}