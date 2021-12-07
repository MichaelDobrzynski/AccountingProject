pipeline {
        agent any

        tools {
            maven "apache-maven 3.6.3"
        }

        stages {
            stage('Build') {
                steps {
                    bat 'mvn clean install'
                }
            }

            stage('Test') {
                steps {
                    bat 'mvn test'
                        step( [ $class: 'JacocoPublisher' ] )
                }
            }

            stage('Deploy') {
                steps {
                    bat 'mvn deploy'
                }
            }
        }
}
