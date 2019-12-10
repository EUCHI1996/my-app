pipeline {
    agent any 
    stages {
        stage('clone repo and clean it') { 
            steps {
                sh "git clone https://github.com/EUCHI1996/my-app.git"
                
                sh "mvn clean -f my-app"
            }
        }
        stage('Test') { 
            steps {
                sh "mvn test -f my-app"
            }
        }
        stage('Deploy') { 
            steps {
                sh "mvn package -f my-app"
            }
        }
    }
}
