pipeline {
    agent any
    stages {
        stage("run frontend"){
            steps {
                echo "exec npm"
                    sh 'npm install'
                    sh 'npm start'
            }    
        }    
    }   
}