pipeline{
    agent any
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