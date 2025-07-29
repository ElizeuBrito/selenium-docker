pipeline{

    agent any

    stages{

        stage('Build Jar'){
            steps{
                sh 'mvn clean package -DskipTests'
            }
        }

        stage('Build Image'){
            steps{
                sh 'docker build -t=157470/selenium:latest .'
            }
        }

        stage('Push Image'){
            steps{
                sh 'docker push 157470/selenium:latest'
            }
        }
    }
}