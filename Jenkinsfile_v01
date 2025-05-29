pipeline {
    agent {
        docker {
            image 'node:16' // Official Node.js image with npm preinstalle
        }
    }
    stages {
        stage('Install Angular CLI') {
            steps {
                sh 'npm install -g @angular/cli@16.2.16'
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('Run Tests') {
            steps {
                sh 'npm test'
            }
        }
        stage('Build Angular App') {
            steps {
                sh 'npx ng build --configuration production'
            }
        }
    }
}
