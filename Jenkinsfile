pipeline {
  agent{label'JDK-JDK'}
  stages{
    stage('vcs') {
      steps{  
        git url: 'https://github.com/sagilechaitanya/spring-petclinic.git',
          branch: 'delclarative' 
      }     
    }
    stage('gradlepackage') {
      steps{         
        sh './gradlew build'
      }    
    }
    stage('sonar') {
      steps{
        withSonarQubeEnv('sonar_cloud'){
          sh './gradlew build sonar:sonar'
        }
      }
    }
    stage('artifactbuild') {
      steps{
        archiveArtifacts artifacts: 'build/libs/**/*.jar', fingerprint: true
        junit 'build/**/**/*.xml'
      }
    }
  }  
  post{
    success{
      mail subject: "Jenkins Build of ${JOB_NAME} with id ${BUILD_ID} is success",
        body: 'send it',
        to: 'sagile@gmail.com'
    }optional refere line 31 
  }
}  
    always{
       archiveArtifacts artifacts: 'build/libs/**/*.jar', fingerprint: true
       junit 'build/**/**/*.xml'
    }
  }
}  


another method to write artifacts
instead of usomg post (always) condition we can use stage


