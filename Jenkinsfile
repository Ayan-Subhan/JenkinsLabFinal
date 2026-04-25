pipeline {
    agent any

    stages {
        agent any
        tools{
            maven 'Maven'
        }
        environment{
            NEW_VERSION ='1.3.0'
        }
        stage('Build') {
            steps {
                echo 'Building..'
                // Here you can define commands for your build
                echo 'Building version $[NEW_VERSION]'
                bat 'nvm install'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing..'
                // Here you can define commands for your tests
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying....'
                // Here you can define commands for your deployment
            }
        }
    }
    post{
        always{
            echo 'Post build condition running'
        }
        faliure{
            echo 'Post Action if Build failed'
        }
    }
    
}
