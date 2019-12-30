pipeline {
    agent any

    stages {
        stage ('Build') {
            steps {
                gradlew('clean', 'classes')
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
