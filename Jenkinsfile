pipeline {
    agent any 
    stages{
        stage("build"){
            steps{
                sh 'mvn clean package'
            }
           }
            
        stage("Docker Build"){
            steps{
                script{
                   docker.build("sample-mavan-app:${TAG}")
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
    
      
