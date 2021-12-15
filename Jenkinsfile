pipeline {
    agent any
    stages {
        stage("git"){
            steps{
                sh 'git pull origin main'
            }

        }
        stage("run frontend"){
            steps {
                echo "exec npm"
                    sh 'npm install'
                    sh 'pm2 restart 0 --update-env'
            }    
        }    
    }   
}