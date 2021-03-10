pipeline {
    agent any 
    stages {
        stage('Build') {
            steps {
                script  {
                    echo "Build step"
                    final String commitMsg = sh (script: 'git log -1', returnStdout: true).trim()
                    echo commitMsg
                    sh 'mvn clean install'
                }
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
