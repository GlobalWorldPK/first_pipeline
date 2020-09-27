pipeline {
         agent any
         stages {
                 stage('Two') {
                     steps {
                     sh 'pip install -r requirements.txt'
                         }
                 }
                 stage('Three') {
                     steps {
                     sh 'python app.py'
                 }
                 }
                 stage('Four') {
                     steps {
                           sh "You are done"
                     }
                 }
              }
}