#!groovy
pipeline {
    options {
        buildDiscarder(logRotator(numToKeepStr: '5'))
        disableConcurrentBuilds()
        timeout(time: 10)
    }
    agent none
    stages {
        stage('Parallel Testing') {
            parallel {
                stage('First Run') {
                    docker { image 'maven:3-alpine' }
                    echo "First stage is running in parallel"
                }
                stage('Second Run') {
                    docker { image 'node:7-alpine' }
                    echo "Second stage is running in parallel"
                }
            }
        }
    }
}
