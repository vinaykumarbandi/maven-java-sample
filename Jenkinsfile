pipeline {
    agent any

    stages{
        stage('Compile') {
            steps {
                bat 'mvn compile'
            }
        }
        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }
        stage('Package') {
            steps {
                bat 'mvn package'
            }
        }
        stage('Deploy') {
            steps {
                bat 'java -jar -Dserver.port=8001 target/spring-petclinic-2.3.1.BUILD-SNAPSHOT.jar'
            }
        }
    }
}
