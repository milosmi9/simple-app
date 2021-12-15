pipeline {
    agent any
    stages {
        stage("dir"){
            steps {
                dir('/home/ec2-user/simple-app'){
                    
                }
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