pipeline {
    agent any 
    stages {
        stage('Build') {
            steps {
                echo "Build step"
                sh 'mvn clean install'
            }
        }
        
        stage('Test') {
            steps {
                echo "Test step"
                sh 'mvn test'
              
            }
        }
        
        stage('Upload artifacts') {
            steps {
                echo 'Run Smart Contract Deployment Pipeline'
                build job: 'demo2'
            }
        }
    }  
}
