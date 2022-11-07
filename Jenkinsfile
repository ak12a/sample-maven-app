pipeline {
    agent any 
    stages{
        stage("build"){
            steps{
                mvn clean package
            }
           }
            
        stage("Docker Build"){
            steps{
                echo "Building Docker image"
                docker build . -t sample-maven-app:${BUILD_NUMBER}
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
    
      
