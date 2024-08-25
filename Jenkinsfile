node ('Open-JDK-11') {
    stage('Version Control') {
        git branch: 'main', changelog: false, poll: false, url: 'https://github.com/thippareddy03/spring-petclinic.git'
    }
    stage('Building the project') {
        build wait: false, propagate: false, job: 'mvn package'
    }
    stage('Archive results') {
        junit '**/surefire-reports/*.xml'
    }
}
