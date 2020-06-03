pipeline {

  agent any
  
  stages{
  
    stage("build") {
    
      steps{
         echo "Hello from: $WORKSPACE"
         sh "./script.sh"
      }
    }
  }
  post{
    always{
      echo "Hello From Post!"
      sh "./failureAdjust.sh"
      archiveArtifacts artifacts: 'response.html'  
    }
  }
}
