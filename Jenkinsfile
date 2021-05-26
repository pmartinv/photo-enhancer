pipeline{
    agent any
    tools {
        maven 'apache-maven-3.8.1' 
    }
    stages{
        stage('build'){
            agent {
                label 'node1'
            }
            steps{
                sh "mvn clean build"
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