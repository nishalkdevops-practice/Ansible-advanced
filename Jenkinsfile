pipeline {
    agent { node { label 'Agent-1'} }

    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }

    stages {

        stage('Trigger') {
            steps {
                echo "Trigger from git with webhook setup"
            }
        }

        stage('build') {
            steps {
                sh 'npm install'
            }
        }
    


        stage('Test') {
            steps {
                echo "Testing happening"
            }
        }

        stage('sonar-scan') {
            steps {
                
                sh ls -lrt
                sh "sonar-scanner"
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