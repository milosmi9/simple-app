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
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: '33dcd16c-4498-4674-b52e-1356788c94d4', url: 'https://github.com/milosmi9/simple-app.git']]])
                echo 'hello git'
                sh 'git fetch'
                sh 'git branch --set-upstream-to origin main'
                sh 'git pull'
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