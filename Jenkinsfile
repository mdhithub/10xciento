pipeline {
    agent any
    stages {
        stage('Clean') {
            steps {
                sh "mvn clean"
            }
        }

        stage('Compile') {
            steps {
                sh "mvn compile"
            }
        }

        stage('Test') {
            steps {
                sh "mvn test"
            }
        }
        
        stage('Test Newman') {
            steps {
                sh "newman run miindicadorTarea.cl.postman_collection.json -n 5"
            }
        }
    }
}
