pipeline {
  agent any
  environment {
  JAVA_HOME = "/usr/bin/java8"
}
  stages {
    stage("Welcome to Jenkins build job") {
      steps {
        script {
          //This section is for input variable
          var1 = input message: 'Enter variable to display', parameters: [string(defaultValue: '10', name: 'var1', trim: true)]
          println "The input variable is ${var1}"

          //This section is for default variables
          println "The job name is ${JOB_NAME}"
        }
      }
    }
  }
}
