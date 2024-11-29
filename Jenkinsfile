pipeline {
    agent { node { label 'Agent-1'} }
    stages {
        stage('build') {
            steps {
                sh 'mvn --version'
            }
        }
    


        stage('Test') {
            steps {
                echo "Testing happening"
            }
        }

        stage('deploy') {
            steps {
                echo "Deployed successfully"
            }
        }
    }

    post{
        always {
            echo "I Will run always if it is failed or success"
        }
        failure {
            echo "I Will run only when it is failure"
        }
        success {
            echo "I Will run only when it is success"
        }
    }
}