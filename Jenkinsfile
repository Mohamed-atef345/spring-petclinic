pipeline {
    agent any

    parameters {
        choice(name: 'mvn_parameters', choices: ['install', 'package', 'test', 'clean'], description: 'mvn parameters choice')
    }
    stages {
        stage('first_stage') {
            steps {
                sh "mvn ${params.mvn_parameters}"
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
