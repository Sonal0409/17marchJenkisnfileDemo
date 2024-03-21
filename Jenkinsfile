pipeline{
    
    tools{
        maven 'mymaven'
    }
    
    // here 'any' means execute pipeline on any available server-> which is current VM for us
    agent any
    
    stages{
        
        stage('Clone Repo'){
            
            steps{
                git 'https://github.com/natmat3017/march17.git'
            }
            
        }
        
        stage('Compile Code'){
    
            steps{
                sh 'mvn compile'
            }
    
    }
    
      stage('Review Code'){
    
            steps{
                sh 'mvn pmd:pmd'
            }
    
    }
    
        stage('Test Code'){
    
            steps{
                sh 'mvn test'
            }
    
    }
    
       stage('Package Code'){
    
            steps{
                sh 'mvn package'
            }
    
    }
    
    
    }
    
    
    
    
    
    
    
}
