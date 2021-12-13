pipeline {
    agent any
    stages {
        stage ("run frontend"){
            echo "exec npm"
            nodejs('Node-17.2.0'){
                sh 'npm install'
                sh 'npm start'
            }
        }    
    }   
}