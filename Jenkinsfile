pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('quality') {
            steps {
                echo 'quality....'
            }
        }
         stage('deploy to dev') {
            steps {
                echo 'deploy to dev'
                
                
            }
}
         stage('deploy to test') {
            steps {
                echo 'deploy to test'
                
                
            }
}


    }
}
