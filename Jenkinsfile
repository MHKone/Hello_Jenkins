pipeline {
    agent any
    stages {  // Move this block one level to the right
        stage('Clone'){
            steps {
                git branch: 'main', url:'https://github.com/MHKone/Hello_Jenkins.git'
            }
        }
    }
}
