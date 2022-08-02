pipeline {
    agent any

    tools { 
      maven 'Maven'
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
         stage('Depoly to Pre_prod') {
            steps {
                echo 'Deploy to Pre_prod'
            }
         
    post {
        always {
            echo 'One way or another, I have finished'
            deleteDir() /* clean up our workspace */
        }
        success {
            echo 'I succeeded!'
        }
        unstable {
            echo 'I am unstable :/'
        }
        failure {
          mail to: 'team@example.com',
             subject: "Failed Pipeline: ${currentBuild.fullDisplayName}",
             body: "Something is wrong with ${env.BUILD_URL}"
        }
        changed {
            echo 'Things were different before...'
        }
    }
}
    }