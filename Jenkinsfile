pipeline {
         agent { docker { image 'python:3.7' } }
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