pipeline {
    agent any

    stages{
        stage('Build'){
            steps{
                sh 'mvn clean install -U -DskipTests'
            }
        }

        stage('Docker Build'){
            steps{
                sh 'docker build -t my-spring-app .'
            }
        }

        stage('Docker Run'){
            steps{
                sh 'docker run -d -p 8080:8080 my-spring-app'
            }
        }

    }
}