pipeline {
  agent any
  stages {
    stage('Build') {
      when {
        expression {
          openshift.withCluster() {
            return !openshift.selector('bc', 'jenkins-demo-os').exists();
          }
        }
      }
      steps {
        script {
          openshift.withCluster() {
            openshift.newApp('redhat-openjdk18-openshift:latest~https://github.com/lucabarze/jenkins-demo.git')
          }
        }
      }
    }
  }
}
