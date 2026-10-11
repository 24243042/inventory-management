
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat 'set "JAVA_HOME=C:\\Users\\Kathavarayan\\AppData\\Local\\Programs\\Eclipse Adoptium\\jdk-21.0.12.101-hotspot" && mvnw.cmd clean compile'
            }
        }

        stage('Test') {
            steps {
                bat 'set "JAVA_HOME=C:\\Users\\Kathavarayan\\AppData\\Local\\Programs\\Eclipse Adoptium\\jdk-21.0.12.101-hotspot" && mvnw.cmd test'
            }
        }

        stage('Package') {
            steps {
                bat 'set "JAVA_HOME=C:\\Users\\Kathavarayan\\AppData\\Local\\Programs\\Eclipse Adoptium\\jdk-21.0.12.101-hotspot" && mvnw.cmd package -DskipTests'
            }
        }
    }

    post {
        success {
            echo 'Inventory Management Build Successful!'
        }
        failure {
            echo 'Build Failed!'
        }
    }
}

