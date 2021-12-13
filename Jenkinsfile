pipeline {
    agent any
    stages {
        stage("run frontend"){
            steps {
                echo "exec npm"
                nodejs('Node-14.18.2) {
                    sh 'npm install'
                    sh 'npm start'
                }
            }    
        }    
    }   
}