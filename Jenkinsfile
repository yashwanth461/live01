pipeline
{
    agent any
    stages {
        stage (git) {
            steps {
                git branch: 'main', url: 'https://github.com/vamsibyramala/live01.git'
            }
        }
        stage (maven) {
            steps {
                sh 'mvn clean package'
            }
        }
        stage (deploy) {
            steps {
                deploy adapters: [tomcat9(credentialsId: 'tomcat', path: '', url: 'http://13.233.148.251:8080/')], contextPath: 'ROOT', war: '**/*.war'
            }
        }
    }
}
