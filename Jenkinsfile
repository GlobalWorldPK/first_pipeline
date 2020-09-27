pipeline {
         agent any
         stages {
                 stage('One') {
                     steps {
                         checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'globalworldpk', url: 'https://github.com/GlobalWorldPK/first_pipeline.git']]])

                     }
                 }
                 stage('Two') {
                     steps {
                            sh "pip install -r requirements.txt"
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