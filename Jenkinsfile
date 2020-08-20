pipeline {
    agent any 
    tools {
        maven "Maven3.6.3"
    }
    stages {
        stage('SCM Checkout') { 
            steps {
                git 
            }
        }
        stage('Compile Package') { 
            steps {
                sh "mvn -version"
                sh "mvn clean install"
                sh "mvn package"
            }
        }
        post{
            always {
                cleanWS()
            }
        }
    }
}
