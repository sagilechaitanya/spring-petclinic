pipeline {
  agent {label 'JDK-JDK'}
  stages {
    stage('vcs') {
      steps {
        git url: 'https://github.com/sagilechaitanya/spring-petclinic.git',
            branch: 'delclarative'
      }
    }
    stage('build') {
      steps {
        sh './mvnw package'
      }
    }
  }
}