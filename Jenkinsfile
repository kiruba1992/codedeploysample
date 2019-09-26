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
        sh 'scp -i /var/jenkins_home/.ssh/id_rsa -r * -p 22 root@10.108.23.122:/opt/'
      }
    }
  }
}