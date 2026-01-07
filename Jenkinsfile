pipeline {
    agent any

    tools {
        gradle 'Gradle'
    }

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking out source code'
            }
        }

        stage('Build') {
            steps {
                echo 'Building project using Gradle'
                bat 'gradle build'
            }
        }

        stage('Run') {
            steps {
                echo 'Running Java application'
                bat 'java -cp build\\classes\\java\\main com.tyit.App'
            }
        }
    }

    post {
        success {
            echo 'Gradle CI Pipeline executed successfully'
        }
        failure {
            echo 'Gradle CI Pipeline failed'
        }
    }
}
