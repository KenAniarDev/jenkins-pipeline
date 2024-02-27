pipeline {
    agent { 
        node {
            label 'docker-agent-alpine'
        }
    }
    environment {
        PATH = "/usr/local/bin:/usr/bin:/bin:/usr/bin/docker:$PATH"
    }
    triggers {
        pollSCM('* * * * *')
    }
    stages {
        stage('Build') {
            steps {
                sh 'echo $PATH'
                sh 'ls'
                sh 'docker -v'
                echo "Jenkins Building Updated.."
                sh '''
                echo "doing build stuff.."
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Jenkins Testing Updated.."
                sh '''
                echo "Doing test stuff.."
                echo "Checking Docker processes..."
                '''
            }
        }
        stage('Deliver') {
            steps {
                echo 'Jenkins Deliver Updated....'
                sh '''
                echo "doing delivery stuff.."
                '''
            }
        }
    }
}
