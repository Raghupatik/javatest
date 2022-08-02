pipeline {
    agent any

    tools { 
      Maven 'Maven'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('code quality') {
            steps {
                echo 'code quality'
            }
        }    
        stage('Depoloy to Dev') {
            steps {
                echo 'depoly to dev'
            }
        }
        stage('Depoly to test') {
            steps {
                echo 'Deploy to test'
            }
        }    
        stage('Depoly to UAT') {
            steps {
                echo 'Deploy to UAT'
            }
        }    
         stage('Depoly to Preprod') {
            steps {
                echo 'Deploy to Preprod'
            }
        }   
         stage('Depoly to prod') {
            steps {
                echo 'Deploy to prod'
            }
        }   
    }
}
