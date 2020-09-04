pipeline {
    agent any

    stages {
        stage('Hello') {    
            steps {
                echo 'Hello World'
            }
            post {
                always {
                    jiraSendBuildInfo branch: 'ECOM-99-issue', site: 'se-demo.atlassian.net'
                }
            }
        }
        stage('Deploy - Dev') {
           
           steps {
               echo 'Deploying to US East Dev 1'
           }
           post {
               always {
                   jiraSendDeploymentInfo site: 'se-demo.atlassian.net', serviceIds: ['ECOM-99','b:YXJpOmNsb3VkOmdyYXBoOjpzZXJ2aWNlLzJlNjQ1Y2Q0LTc4ZmEtMTFlYS04ZjMyLTBhNzdmM2Y0NTMwNC8xNWM3YmZjYy1lZWI2LTExZWEtOWFmZC0xMjhiNDI4MTk0MjQ='], environmentId: 'us-prod-1', environmentName: 'us-prod-1', environmentType: 'production'
               }
           }
        }
    }
}
