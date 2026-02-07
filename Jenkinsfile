pipeline {
    agent any

    tools {
        nodejs 'nodejs'   // Jenkins > Global Tool Configuration ch NodeJS name
    }

    environment {
        NODE_ENV = 'any'
    }

    stages {

        stage('Checkout Code') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/eshuramgarhia/tour-repo.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                bat 'npm install'
            }
        }

        stage('Run Tests') {
            steps {
                bat 'npm test'
            }
        }

    }
  }
