pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package -DskipTests'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'sudo docker build -t my-spring-app .'
            }
        }

        stage('Docker Run') {
            steps {
                sh 'sudo docker run -d -p 8080:8080 my-spring-app'
            }
        }
    }
}
