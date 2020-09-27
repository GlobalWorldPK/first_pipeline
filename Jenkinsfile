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
                         node('label'){
                                // now you are on slave labeled with 'label'
                                def workspace = WORKSPACE
                                // ${workspace} will now contain an absolute path to job workspace on slave

                                workspace = env.WORKSPACE
                                // ${workspace} will still contain an absolute path to job workspace on slave

                                // When using a GString at least later Jenkins versions could only handle the env.WORKSPACE variant:
                                echo "Current workspace is ${env.WORKSPACE}"

                                // the current Jenkins instances will support the short syntax, too:
                                echo "Current workspace is $WORKSPACE"

                            }
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