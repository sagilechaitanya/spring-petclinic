pipeline{
  agent {label'maven'}
  stages{
    stage('vcs') {
      steps{
        git url: 'https://github.com/sagilechaitanya/spring-petclinic.git',
            branch: jenkins
      }
    }
    stage('build') {
      steps{
        sh './mvnw package'
      }
    }
  }
}


























node ('JDK-JDK') {
      stage('vcs') {
        git url: 'https://github.com/sagilechaitanya/spring-petclinic.git',
            branch: 'jenkins'
      }  
      stage('build') {
        sh './mvnw package'
      }
    }  
