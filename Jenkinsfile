pipeline {
    agent any

    tools {
        maven 'Maven3'
    }

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/ratakondadimpul/MVN_03.git'
            }
        }

        stage('Package') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Run JAR') {
            steps {
                sh 'java -cp target/maven-package-demo-1.0.jar com.example.App'
            }
        }
    }
}