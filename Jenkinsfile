pipeline {
  agent any
  stages {
    stage('Check Out') {
      steps {
        git(url: 'https://github.com/GlobalWorldPK/first_pipeline.git', branch: 'master')
      }
    }

    stage('Build') {
      steps {
        sh "python first_script.py"
      }
    }

    stage('Run') {
      steps {
        echo 'Hello.'
      }
    }

  }
}