#!groovy
node {
//    parallel {
        stage('First Run') {
            docker.image('ubuntu').pull() {
                echo "First stage is running in parallel"
            }
        }
        stage('Second Run') {
            docker.image('redhat/ubi8-minimal').pull() {
                echo "Second stage is running in parallel"
            }
        }
//    }
}
