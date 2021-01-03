pipeline {
  agent any
  stages {
    stage('Dev Build') {
      steps {
        echo 'Dev Build to Start'
        git(url: 'https://github.com/GopinathJayakumar/spring-petclinic', branch: 'master', poll: true)
        bat(script: 'mvnw package', label: 'Dev')
      }
    }

    stage('Smoke Test') {
      steps {
        echo 'Smoke Test to start'
      }
    }

  }
}