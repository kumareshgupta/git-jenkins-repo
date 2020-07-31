pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
		sh mvn 'test'
		input('Do you want to continue now?')
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
		sh mvn 'clean install'
            }
        }
    }
}
