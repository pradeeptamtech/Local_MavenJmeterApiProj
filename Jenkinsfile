pipeline {

    agent any
   // tools {
   //     maven 'Maven_3.6.3' 
   // }
    stages {
        stage('Compile stage') {
            steps {
                bat "mvn clean" 
        }
    }

         stage('testing stage') {
             steps {
                bat "mvn install"
        }
    }

         // stage('deployment stage') {
         //     steps {
         //       bat "mvn deploy"
       // }
    //}

  }

}
