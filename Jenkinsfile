pipeline{
    agent any
    stages{
        stage("A"){
            steps{
                git 'https://github.com/phuongvd7/spring-petclinic.git'
            }
        }
        stage('Build') {
            steps {
                // Perform the build steps
                sh 'mvn clean install'
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