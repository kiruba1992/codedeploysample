pipeline {
  agent any
  stages {
    stage('deploy') {
      steps {
        sh 'scp  -i "$pvt_key" -P 22 -rv Jenkinsfile  root@10.108.23.122:/'
      }
    }
  }
  environment {
    pvt_key = '/var/jenkins_home/.ssh/id_rsa'
  }
}