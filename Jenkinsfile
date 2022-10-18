pipeline{
    agent any
    tools {
        maven 'mavenBuild'
    }

    stages{
        stage("Maven testing stage "){
            steps{ 
                sh '''
                mvn -version 
                '''
                echo "========testing A========"
            }
            
        }
        stage("Maven compile stage"){
           input {
            message "Should we continue ?"
            ok "yes we should "
           }
            steps{
                echo "========compile A========"
            }
        }
        stage("Maven build stage package"){
            steps{
                echo "========building A========"
            }
        }
        stage("Deploy on server testing one "){
            steps{
                echo "========deploy on testing A========"
            }
        }
        stage("Deploy on prod server"){
            steps{
                echo "deploy on prod server"
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
