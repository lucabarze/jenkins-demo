pipeline {
    agent any
    tools {
        maven 'Maven 3.6.3'
        jdk 'jdk8'
    }

    stage('Checkout') {
        git 'https://github.com/lucabarze/jenkins-demo'
    }

    stage ('Build') {
        sh 'mvn clean package' 
    }
}
