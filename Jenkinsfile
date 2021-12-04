pipeline {
        agent any

        tools {
            maven "apache-maven 3.6.3"
        }

        stages {
            stage('Build') {
                steps {
                    sh 'mvn clean install'
                }
            }

            stage('Test') {
                steps {
                    sh 'mvn test'
                }
            }

            stage('Deploy') {
                steps {
                    sh 'mvn deploy'
                }
            }
        }
}
