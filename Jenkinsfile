pipeline{
    agent { node { label 'node_slave' } }
    stages{
        stage("A"){
            steps{
                git branch: 'main', url: 'https://github.com/phuongvd7/spring-petclinic.git'
            }
        }
        stage('Build') {
            steps {
                // Perform the build steps
                sh './mvnw package' 
                sh 'java -jar target/*.jar' 
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