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
}