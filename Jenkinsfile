pipeline {
  agent any
  stages {
    stage('Dev Build') {
      steps {
        echo 'Dev Build to Start'
        git(url: 'https://github.com/GopinathJayakumar/spring-petclinic', branch: 'master', poll: true)
        powershell(script: 'mvnw install', label: 'Dev')
        powershell 'java -jar target/*.jar'
      }
    }

    stage('Smoke Test') {
      steps {
        echo 'Smoke Test to start'
      }
    }

  }
}