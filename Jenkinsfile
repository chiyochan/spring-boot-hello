@Library('standard@master') _
pipeline {
    agent any

    parameters {
        string(name:'PERSON', defaultValue:'', description:'default user')
        text(name:'EMAILS', defaultValue:'', description:'send emails to whom')
        booleanParam(name:'JIRA', defaultValue:'', description:'Should we update JIRA')
        choice(name:'SCAN_TYPE', choices:['BLACKDUCK','CHECKMARX'], description:'Which scans should we run?')
        password(name:'PASSWORD', defaultValue:'', description:'Default password to access services')

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
                standard()
            }

        }

        stage ('Test') {
            steps {
                echo "Test"
                // bat 'gradle test'
            }

        }

        stage ('Deploy') {
            steps {
                echo "Deploy"
                // bat 'java -jar -Dserver.port=8083 build/libs/gs-spring-boot-0.1.0.jar --server-port=8083'
                // bat 'curl localhost:8083/actuator/health'
            }

        }


    }
    }
