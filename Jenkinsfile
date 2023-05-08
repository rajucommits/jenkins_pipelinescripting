pipeline {
  agent any
  environment {
  JAVA_HOME = "/usr/bin/java8"
  }

  parameters {
  choice choices: ['dev', 'sit', 'prod', 'uat'], description: 'environment choices', name: 'ENV'
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

          //This section is of environment variables
          println "The java path is ${JAVA_HOME} without specifying env"
          println "The java path is ${env.JAVA_HOME} with specifying env"

          //This section is of parameter variables
          println "The chosen environment is ${ENV}, without specifying params"
          println "The chosen environment is ${params.ENV}, with specifying params"

          //Working with if condition
          a = 10
          b = 20

          if (a>b) {println "a=${a} is big"}
          else {println "b=${b} is big"}


          //working with for loop
          for (i=1;i<=3;i++) {println "1st way in for loop, i is ${i}"}
          //another way of defining for loop
          lis1 = [10,20,20]
          for (i in lis1) {println "2nd way in for loop, i is ${i}"}


          //working with while loop
          j=1
          while (j<=3) {
            println "while loop, j is ${j}"
            sleep(2)
            j++
          }
        }
      }
    }
  }
}
