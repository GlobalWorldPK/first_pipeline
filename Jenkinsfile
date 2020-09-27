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
                            def Foldername = JOB_NAME;
                            def theString = "<a href='https://jenkins.com/job/" + Foldername + "/" + BUILD_NUMBER + "/execution/node/3/ws/'>Workspace</a>";
                            sh "cd theString"
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