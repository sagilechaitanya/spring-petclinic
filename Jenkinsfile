pipeline {
  agent (chaitanya) {
    stages {
      stage (vcs) {
        git url: https://github.com/sagilechaitanya/spring-petclinic.git,
            branch: jenkins

      }  
      stage (build) {
        sh ./mvnw package
      }
    }
  }  
}