pipeline {

    agent any
    tools {
        maven 'Maven_3.6.3' 
    }
    stages {
        stage('Compile stage') {
            steps {
                bat "mvn clean compile" 
        }
    }

         stage('testing stage') {
             steps {
                bat "mvn test"
        }
    }

         // stage('deployment stage') {
         //     steps {
        //        bat "mvn deploy"
       // }
    //}
        
        stage("Email") {
            steps{
                    emailext( to:'pradeepta.panigrahi@hp.com' ,
                              replyTo:'pradeeptamtech@gmail.com',
                              subject: "Email Report from- '${env.JOB_NAME}'",
                              //body: readFile("target/reports/"),
                              mimeType: 'text/html' );
                }
         }    
        
        
       // post {
        //      always {
       //                mail to: 'pradeepta.panigrahi@hp.com',
       //                subject: "Status of pipeline: ${currentBuild.fullDisplayName}",
       //                body: "${env.BUILD_URL} has result ${currentBuild.result}"
      //               }
       //        }

  }

}
