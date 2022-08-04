pipeline {
    agent any

    tools { 
      maven 'Maven'
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
          }
      
        stage('Test') {
            steps {
                 echo "${env.BUILD_NUMBER}"
                 echo "${env.BUILD_URL}"
            }
        }
        stage('Code Quality') {
            steps {
                echo 'Quality'
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
                echo 'Staging'
            }
         }
         stage('Prod approval') {
           steps {
            script {
                if (env.BRANCH_NAME == "master") {
                    input ('proceed for prod deployment ?')
                 }
              }
           }
         }     
        stage('Depoly to prod') {
          steps {
                echo 'prod'
            }   
            post {
              failure{
                echo 'sending notifications'
              }
            }
        }
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