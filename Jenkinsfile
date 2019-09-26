pipeline {
  agent any
  stages {
    stage('prebuild') {
      steps {
        git(url: 'https://github.com/kiruba1992/Ansible_Cloudwatchlogsagent_Install_PB.git', branch: 'master')
      }
    }
    stage('deploy') {
      steps {
        sh 'scp  -i "$pvt_key" -rv Jenkinsfile -P 22 root@10.108.23.122:/'
      }
    }
  }
  environment {
    pvt_key = '/var/jenkins_home/.ssh/id_rsa'
  }
}