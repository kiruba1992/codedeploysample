pipeline {
  agent any
  stages {
    stage('prebuild') {
      steps {
        git(url: 'https://github.com/kiruba1992/Ansible_Cloudwatchlogsagent_Install_PB.git', branch: 'master')
      }
    }
    stage('build') {
      steps {
        sh '''echo " $pass "





'''
      }
    }
  }
  environment {
    pass = 'credentials(\'pass\')'
  }
}