pipeline {
         agent any
         stages {
                 stage('One') {
                     steps {
                         checkout scm
                     }
                 }
                 stage('Two') {
                     steps {
                     sh 'pip install -r requirements.txt'
                         }
                 }
                 stage('Three') {
                     steps {
                     sh 'python app.py'
                 }
                 stage('Four') {
                     steps {
                           sh "You are done"
                     }
                 }
              }
}