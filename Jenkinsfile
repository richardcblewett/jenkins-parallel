#!/groovy
pipeline {
    agent none
    stages {
        stage('Parallel Testing') {
            parallel {
                stage('First Run') {
                    agent {
                        docker { image 'maven:3-alpine' }
                    }
                    steps {
                        echo "First stage is running in parallel"
                    }
                    }
                }
                stage('Second Run') {
                    agent {
                        docker { image 'node:7-alpine' }
                    }
                    steps {
                        echo "Second stage is running in parallel"
                    }
                    }
                }
            }
        }
    }
}
