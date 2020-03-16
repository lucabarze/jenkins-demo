pipeline {
    agent any
    tools {
        maven 'Maven 3.6.3'
        jdk 'jdk8'
    }
    stages {
        stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                '''
            }
        }

        stage('Checkout') {
            git 'https://github.com/bertjan/spring-boot-sample'
        }

        stage ('Build') {
            steps {
                sh 'mvn package' 
            }
        }
    }
}
