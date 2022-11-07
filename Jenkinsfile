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
                   docker.build("${DOCKER_IMAGE}:${BUILD_NUMBER}")
                }
            }
        }
        stage("Image Vulnerability Scan  "){
            steps{
                sh "trivy image --severity CRITICAL ${DOCKER_IMAGE}:${BUILD_NUMBER}"
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
   


    
      
