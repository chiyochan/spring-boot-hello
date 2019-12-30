pipeline {
    agent any

    stages {
        stage ('Build') {
            steps {
                gradle('clean', 'classes')
            }

        }

        stage ('Test') {
            steps {
                echo "Test"
            }

        }

        stage ('Deploy') {
            steps {
                echo "Deploy"
            }

        }


    }
    }
