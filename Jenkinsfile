pipeline {
    agent any
    stages {
        stage("dir"){
            steps {
                sh "pwd"
                dir('simple-app') {
                    sh "pwd"
                }
                sh "pwd"
            } 
        }
        stage("git"){
            steps{

                sh 'git pull origin main'
            }

        }
        stage("run frontend"){
            steps {
                echo "exec npm"
                    sh 'npm install'
                    sh 'pm2 restart all'
            }    
        }    
    }   
}