pipeline {
  agent {label 'JDK-JDK'}
  stages{
      stage('vcs') {
        git url: 'https://github.com/sagilechaitanya/spring-petclinic.git',
            branch: 'delcarative'
      }  
      stage('build') {
        sh './mvnw package'
      }  
  }
}
