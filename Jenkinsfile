def label = "mypod-${UUID.randomUUID().toString()}"
def label2 = "jenkins-pipeline"
echo 'Start pipeline...'
println label
echo label
println label2
echo label2
podTemplate(label: label2, containers: [
    containerTemplate(name: 'maven', image: 'maven:3.3.9-jdk-8-alpine', ttyEnabled: true, command: 'cat'),
    containerTemplate(name: 'golang', image: 'golang:1.8.0', ttyEnabled: true, command: 'cat')
  ]) {

    node(label2) {
        stage('stage 1') {
            sh """
            echo 'stage 1'
            """
        }

        stage('stage 2') {
            sh """
            echo 'stage 2'
            """
        }
    }
}