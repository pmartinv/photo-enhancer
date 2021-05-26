pipeline{
    agent any
    tools {
        maven 'maven-3.8.1' 
    }
    stages{
        stage('build'){
            agent {
                label 'node1'
            }
            steps{
                sh "mvn clean compile"
            }
        }
        stage('test'){
            agent {
                label 'node2'
            }
            steps{
                sh "mvn clean test"
            }
        }

    }
}