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
      emailtext(
        subject: "Email From Build!",
        body: "Hi There",
        to: "jonas.meier@ergon.ch",
        from: "HeyItsMe@jenkins"
      )        
    }
  }
}
