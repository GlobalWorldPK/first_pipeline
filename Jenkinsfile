pipeline {
         agent any
         stages {
                 stage('One') {
                     steps {
                         sh 'git clone https://github.com/GlobalWorldPK/first_pipeline.git'

                     }
                 }
                 stage('Two') {
                     steps {
                        sh 'cd first_pipeline1'
                     }
                 }
                 stage('Three') {
                     steps {
                          image = sh 'docker build first_pipeline1'
                     }
                 }
                 stage('Four') {
                     steps {
                           sh "docker run "+image
                     }
                 }
              }
}