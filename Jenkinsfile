pipeline {
    agent any
    tools {nodejs "node"}
    stages{
        
        stage('Git') {
            steps {
                git branch: '' , url: ''
            }
        }

        stage('Install') {
            steps { sh 'npm install'}
        }

        stage('Test') {
            steps { sh 'npm run test --watch=false'}
        }

        stage('Build'){
            steps { sh 'npm run ng build --configuration="production" --optimization --build-optimizer' }
        }

        stage('Deploy'){
            steps{ sh 'mv dist/ProyectoFinalQA/* /home'}
        }
    }
}