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
      script{
        if(params.branch_NAME == 'master'){
          echo "Hello From master!"
          sh "./failureAdjust.sh"
          archiveArtifacts artifacts: 'response.html' 
      }
    }
  }
}
