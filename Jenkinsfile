pipeline {
    agent any 
    tools {
        maven "Maven3.6.3"
    }
    stages {
        stage('SCM Checkout') { 
            steps {
                git "https://github.com/Oishi2000/my_app_maven.git"
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
