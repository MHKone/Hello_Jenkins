pipeline {
    agent any
    stages {  // Move this block one level to the right
        stage('Clone'){
            steps {
                git branch: 'main', url:'https://github.com/MHKone/Hello_Jenkins.git'
            }
        }
        stage('Build Image'){
            steps {
                withDockerRegistry(credentialsId: 'f8868f54-a536-41e1-9452-7adf4142ae52', url: 'https://index.docker.io/v1/') {
                    sh 'docker build -t mhkone113/jenkins_image:v1.0.'
                    sh 'docker push -t mhkone113/jenkins_image:v1.0.'
                }
            }

        }
    }
}
