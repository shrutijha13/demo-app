pipeline {
    agent any 
    stages {
        stage('Build') {
            steps {
                echo "Build step"
                sh 'mvn -Dmaven.test.failure.ignore=true install'
            }
        }
        
        stage('Test') {
            steps {
                echo "Test step"
                sh 'mvn tests'
              
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
