pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
               bat "rmdir  /s /q Jenkins1"
                bat "git clone https://github.com/Warhawk9135/Jenkins1.git"
                bat "mvn clean -f Jenkins1"
            }
        }
        stage('install') {
            steps {
                bat "mvn install -f Jenkins1"
            }
        }
        stage('test') {
            steps {
                bat "mvn test -f Jenkins1"
            }
        }
        stage('package') {
            steps {
                bat "mvn package -f TicketBookingServiceJunitTesting"
            }
        }
    }
}
