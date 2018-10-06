def label = "mypod-${UUID.randomUUID().toString()}"
println label
podTemplate(label: label, containers: [
    containerTemplate(name: 'maven', image: 'maven:3.3.9-jdk-8-alpine', ttyEnabled: true, command: 'cat'),
    containerTemplate(name: 'golang', image: 'golang:1.8.0', ttyEnabled: true, command: 'cat')
  ]) {

    node(label) {
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