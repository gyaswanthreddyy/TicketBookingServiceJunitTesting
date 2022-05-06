pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
                ///bat "rmdir  /s /q TicketBookingServiceJunitTesting"///
                sh "git clone https://github.com/gyaswanthreddyy/TicketBookingServiceJunitTesting.git"
                sh "mvn clean -f TicketBookingServiceJunitTesting"
            }
        }
        stage('install') {
            steps {
                sh "mvn install -f TicketBookingServiceJunitTesting"
            }
        }
        stage('test') {
            steps {
                sh "mvn test -f TicketBookingServiceJunitTesting"
            }
        }
        stage('package') {
            steps {
                sh "mvn package -f TicketBookingServiceJunitTesting"
            }
        }
    }
}
