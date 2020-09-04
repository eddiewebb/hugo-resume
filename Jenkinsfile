pipeline {
    agent any

    stages {
        stage('Hello') {    
            steps {
                echo 'Hello World'
            }
            post {
                always {
                    jiraSendBuildInfo site: 'se-demo.atlassian.net'
                }
            }
        }
        stage('Deploy - Dev') {
           
           steps {
               echo 'Deploying to US East Dev 1'
           }
           post {
               always {
                   jiraSendDeploymentInfo site: 'se-demo.atlassian.net', serviceIds: ['b:YXJpOmNsb3VkOmdyYXBoOjpzZXJ2aWNlLzJlNjQ1Y2Q0LTc4ZmEtMTFlYS04ZjMyLTBhNzdmM2Y0NTMwNC8xNWM3YmZjYy1lZWI2LTExZWEtOWFmZC0xMjhiNDI4MTk0MjQ='], environmentId: 'us-dev-1', environmentName: 'us-dev-1', environmentType: 'development'
               }
           }
        }
        /* waiting on plugin update
        stage('Deploy - prod') {
                steps {
                    echo 'Queueing...'
                    jiraSendDeploymentInfo(site:'se-demo.atlassian.net',
                            environmentId:'us-prd-1',
                            environmentName:'us-prd-1',
                            environmentType:'production',
                            // now we can define a state of build explicitly
                            state:"pending",
                            enableGate:true,
                            serviceIds: [
                    "b:YXJpOmNsb3VkOmdyYXBoOjpzZXJ2aWNlLzJlNjQ1Y2Q0LTc4ZmEtMTFlYS04ZjMyLTBhNzdmM2Y0NTMwNC8xNWM3YmZjYy1lZWI2LTExZWEtOWFmZC0xMjhiNDI4MTk0MjQ="]
                        )
                }
            }
            stage("check gate") {
                steps {
                    waitUntil {
                        input message: "Check for approval?"
                        checkGateStatus(site:'se-demo.atlassian.net', environmentId:'us-prd-1')
                    }
                }
            }
            stage("deploy") {
                steps {
                    echo "Deploying!"
                }
            }
            */
    }
}
