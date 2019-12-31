pipeline {
    agent any

    parameters {
        string(name:'PERSON', defaultValue:'JANE', description:'default user')
        text(name:'EMAILS', defaultValue:'JANE@gmail.com', description:'send emails to whom')
        booleanParam(name:'JIRA', defaultValue:'YES', description:'Should we update JIRA')
        choice(name:'SCAN_TYPE', defaultValue:['BLACKDUCK','CHECKMARX'], description:'Which scans should we run?')
        password(name:'PASSWORD', defaultValue:'PASS123', description:'Default password to access services')

    }

    stages {

        stage ('Init') {
            steps {
                echo "${params.PERSON}"
                echo "${params.EMAILS}"
                echo "${params.JIRA}"
                echo "${params.SCAN_TYPE}"
                echo "${params.PASSWORD}"

            }

        }

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
