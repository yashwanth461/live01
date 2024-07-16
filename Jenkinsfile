node {
    stage('SCM') {
        git branch: 'main', url: 'https://github.com/vamsibyramala/live01.git'
    }
    stage('Build') {
        sh 'mvn clean package'
    }
}
