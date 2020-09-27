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
                        sh 'cd first_pipeline1'
                     }
                 }
                 stage('Three') {
                     steps {
                          sh 'docker build first_pipeline1'
                     }
                 }
                 stage('Four') {
                     steps {
                           sh "docker run first_pipeline1"
                     }
                 }
              }
}