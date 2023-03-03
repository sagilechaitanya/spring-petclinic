pipeline {
  agent {label 'JDK-JDK'}
  stages {
    stage('vcs') {
      steps {
        git url: 'https://github.com/sagilechaitanya/spring-petclinic.git',
            branch: 'declarative'
      }
    }
    stage('build') {
      steps {
        sh './mvnw package'
      }
    }
  }
}