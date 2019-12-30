pipeline {
    agent any

    stages {
        stage ('Build') {
            steps {
                bat 'gradle clean build'
            }

        }

        stage ('Test') {
            steps {
                bat 'gradle test'
            }

        }

        stage ('Deploy') {
            steps {
                bat 'java -jar -Dserver.port=8083 build/libs/gs-spring-boot-0.1.0.jar --server-port=8083'
                bat 'curl localhost:8083/actuator/health'
            }

        }


    }
    }
