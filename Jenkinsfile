pipeline {
    agent any 
    stages{
        stage("build"){
            steps{
                sh 'mvn  package'
            }
           }
            
        stage("Docker Build"){
            steps{
                script {
                   docker.build("sample-mavan-app:${BUILD_NUMBER}")
                }
            }
        }
        stage("C"){
            steps{
                echo "========executing C========"
            }                            
          }
        }
    post{
      always{
          echo "========always========"
      }
      success{
          echo "========pipeline executed successfully ========"
      }
      failure{
          echo "========pipeline execution failed========"
      }
     }
   }        
   


    
      
