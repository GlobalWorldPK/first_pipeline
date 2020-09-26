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
        build 'first_script.py'
      }
    }

    stage('Run') {
      steps {
        echo 'Hello.'
      }
    }

  }
}