#!groovy
node {
    parallel (
           'one': {stage('First Run') {
//            docker.image('ubuntu') {
            echo "First stage is running in parallel"
//            }
        }},
            'two': {stage('Second Run') {
//            docker.image('redhat/ubi8-minimal') {
            echo "Second stage is running in parallel"
//            }
        }}
    )
}
