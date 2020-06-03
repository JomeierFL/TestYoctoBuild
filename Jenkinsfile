pipeline {

  agent any
  
  stages{
  
    stage("build") {
    
      steps{
         echo "Hello from: $WORKSPACE"
         echo "Changes"
         sh "./script.sh"
      }
    }
  }
  post{
    always{
      script{
        if(1 == 1){
          echo "Hello From master!"
          sh "./failureAdjust.sh"
          archiveArtifacts artifacts: 'response.html'
        }
      }
    }
  }
}
