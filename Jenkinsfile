
pipeline {
	agent any
  stages {
  	stage('Checkout') {
    	
      git url :'https://github.com/polotacki/jgsu-spring-petclinic.git'
                branch:'main'
        }
  }
      
    
    stage(Build') {
    	sh './mvnw clean package'
    }
          post{
                  always{
                  junit'**/target/surefire-reports/TEST-*.xml'
                          archiveArtifacts 'target/*.jar'
                  
                  }
          }
  }
}
