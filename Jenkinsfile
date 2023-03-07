pipeline {
  agent{label'gradle'}
  stages{
    stage('vcs') {
      steps{  
        git url: 'https://github.com/sagilechaitanya/spring-petclinic.git',
          branch: 'gradele' 
      }     
    }
    stage('gradlepackage') {
      steps{         
        sh './gradlew build'
      }    
    }
  }
  post{
    success{
      mail subject: "Jenkins Build of ${JOB_NAME} with id ${BUILD_ID} is success",
        body: 'send it',
        to: 'sagile@gmail.com'
      
    }
  }
}