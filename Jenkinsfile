pipeline {
    agent any

    tools {
        jdk 'jdk21'
        nodejs 'node20'
    }

    stages {

        stage('Clone Code') {
            steps {
                git branch: 'main',
                url: 'https://github.com/Vishal-git-hub29/Full-stack-Employee-Management-System-using-SpringBoot-and-React-Js-.git'
            }
        }

        stage('Build Backend') {
    steps {
        dir('ems-backend/ems-backend') {
            sh 'chmod +x mvnw'
            sh './mvnw clean install'
        }
    }
}

        stage('Build Frontend') {
            steps {
                dir('ems-fullstack') {
                    sh 'npm install'
                    sh 'npm run build'
                }
            }
        }
    }
}