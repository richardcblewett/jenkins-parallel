#!groovy
node {
    stage('Parallel Testing') {
        parallel {
            stage('First Run') {
                docker.image('maven:3-alpine') {
                    echo "First stage is running in parallel"
                }
            }
            stage('Second Run') {
                docker.image('node:7-alpine') {
                    echo "Second stage is running in parallel"
                }
            }
        }
    }
}
