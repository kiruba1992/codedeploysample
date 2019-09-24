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
        sh 'echo " $git_branch "'
      }
    }
    stage('postbuild') {
      steps {
        sh '''docker -version



'''
      }
    }
  }
  environment {
    name = 'staging'
  }
}