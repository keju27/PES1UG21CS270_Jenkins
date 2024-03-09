pipeline{
    agent any
    stages {
        stage('Build'){
            steps{
                build 'PES1UG21CS270-1'
                sh 'g++ main.cpp -o output'
                echo 'build Stage Scccessful'

            }
        }
        stage('Test'){
            steps{
                sh './output'
                echo 'Test Stage Successful'
            }
        }
        stage('Deploy'){
            steps{
                echo 'Deployment Sucessful'
            }
        }
        post{
            failure{
                error 'Pipeline failed'
            }
        }
    }
}