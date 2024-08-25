node('Open-JDK-11') {
    stage('Version Control') {
        git branch: 'main', url: 'https://github.com/thippareddy03/spring-petclinic.git'
    }
    stage('Building Project') {
        sh 'mvn package'
    }
    stage('Unit Tests') {
        junit '**/surefire-reports/*.xml'
    }
}