pipeline {
    agent any

    stages {
        stage('Hello') {
            git 'https://github.com/eddiewebb/hugo-resume.git'
    
            steps {
                echo 'Hello World'
            }
            post {
                always {
                    jiraSendBuildInfo site: 'se-demo.atlassian.net'
                }
            }
        }
        stage('Deploy - Production') {
           when {
               branch 'master'
           }
           steps {
               echo 'Deploying to Production from master...'
           }
           post {
               always {
                   jiraSendDeploymentInfo site: 'se-demo.atlassian.net', serviceIds: ['b:YXJpOmNsb3VkOmdyYXBoOjpzZXJ2aWNlLzJlNjQ1Y2Q0LTc4ZmEtMTFlYS04ZjMyLTBhNzdmM2Y0NTMwNC8xNWM3YmZjYy1lZWI2LTExZWEtOWFmZC0xMjhiNDI4MTk0MjQ='], environmentId: 'us-prod-1', environmentName: 'us-prod-1', environmentType: 'production'
               }
           }
}
    }
}
