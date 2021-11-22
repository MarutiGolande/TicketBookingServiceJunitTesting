pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
                //bat "git clone https://github.com/MarutiGolande/TicketBookingServiceJunitTesting.git"
                sh "git pull"
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
