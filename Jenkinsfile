pipeline {
    agent any

    tools {
        nodejs 'NodeJS'   // Jenkins > Global Tool Configuration ch NodeJS name
    }

    environment {
        NODE_ENV = 'NodeJS 18.1.0'
    }

    stages {

        stage('Checkout Code') {
            steps {
                git branch: 'master',
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
