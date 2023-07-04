pipeline{
    
    tools{
        maven 'mymaven'
    }
    
    agent any 
    
    stages{
        stage('clone reop'){
            steps{
                // give any comment
                git 'https://github.com/Sonal0409/DevOpsClassCodes.git'
            }
        }
        stage('compile code'){
            steps{
                sh 'mvn compile'
            }
        }
        stage('Code review'){
            steps{
                sh 'mvn pmd:pmd'
            }
        }
        stage('Test'){
            steps{
                sh 'mvn test'
            }
        }
        stage('package'){
            steps{
                sh 'mvn package'
            }
        }
    }
}
