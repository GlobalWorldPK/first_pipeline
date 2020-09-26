pipeline {
  agent any
  stages {
    stage('Check Out') {
      steps {
        checkout scm
      }
    }

    stage('Build') {
         steps {
      script {
          sh """
          pip install -r requirements.txt
          """
        }
        }
    }

    stage('Run') {
      steps {
        script {
          sh """
          python first_script.py
        """
      }
      }
    }

  }
}