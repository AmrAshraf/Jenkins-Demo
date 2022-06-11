pipeline {
  agent any
  
  environment{
    NEW_VERSION = "1.1.0" 
  }
  stages {
  
    stage("build") {
    
      steps {
        echo "build step started with build version: ${NEW_VERSION}"
      
      }
    
    }
  
    stage("test") {
    
      when{
          expression {
              BRANCH_NAME == "dev"
          }
      }
      steps {
        echo "test step started with build version: ${NEW_VERSION}"
      
      }
    
    }
    stage("deploy") {
    
      steps {
        echo "deploy step started with build version: ${NEW_VERSION}"
      
      }
    
    }
  
  }

  post {
    always {
     echo "post always message" 
    }
    success {
      echo "post success message"
    }
    
    failure {
      echo "post failure message"
    }
    
  }



}
