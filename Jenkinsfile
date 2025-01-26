pipeline {
    agent any

    stages {
        stage('source') {
            steps {
                echo 'Hello World'
                git branch: 'main', url: 'https://github.com/spring-projects/spring-petclinic.git'
            }
        }
        stage('package') {
            steps {
                sh 'mvn package'
            }
        }
        stage('test') {
            steps {
                sh 'mvn test'
            }
        }
    }
}
