pipeline {
    agent any

    stages {
        stage('first_stage') {
             parameters {
                    string(name: 'mvn_parameter', defaultValue: 'install', description: 'mvn_parameter')
                }
            steps {
                sh "mvn ${mvn_parameter}"
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
