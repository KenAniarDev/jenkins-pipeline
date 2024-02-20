pipeline {
    agent { 
        node {
            label 'docker-agent-alpine'
            }
      }
    triggers {
        pollSCM('* * * * *')
    }
    stages {
        stage('Build') {
            steps {
                echo "Jenkins Building.."
                sh '''
                echo "doing build stuff.."
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Jenkins Testing.."
                sh '''
                echo "doing test stuff.."
                '''
            }
        }
        stage('Deliver') {
            steps {
                echo 'Jenkins Deliver....'
                sh '''
                echo "doing delivery stuff.."
                '''
            }
        }
    }
}