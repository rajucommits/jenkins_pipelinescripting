pipeline {
  agent any
  stages {
    stage("Welcome to Jenkins build job") {
      steps {
        script {
          var1 = input message: 'Enter variable to display', parameters: [string(defaultValue: '10', name: 'var1', trim: true)]
          println "The input variable is ${var1}"
        }
      }
    }
  }
}
