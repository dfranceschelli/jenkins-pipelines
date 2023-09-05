pipeline {
    
    tools {
        maven "maven 3.9.4"
    }
    
    agent any
    
    stages {
        
        stage("Clone repo") {
            
            steps {
                git 'https://github.com/Sonal0409/DevOpsCodeDemo.git'
            }
        }
        
        stage("Review Code") {
            
            steps {
                sh "mvn pmd:pmd"
            }
        }
        
        stage("Compile Code") {
            steps {
                sh "mvn compile"
            }
        }
        
        stage("Test Code") {
            
            steps {
                sh "mvn test"
            }
        }
        
        stage("Package Code") {
            steps {
                sh "mvn package"
            }
        }
    }
}
