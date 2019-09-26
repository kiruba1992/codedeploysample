pipeline {
  agent any
  stages {
    stage('prebuild') {
      steps {
        git(url: 'https://github.com/kiruba1992/Ansible_Cloudwatchlogsagent_Install_PB.git', branch: 'master')
      }
    }
    stage('cred_set') {
      steps {
        sh 'withCredentials(bindings: [sshUserPrivateKey(credentialsId: \'89a7299b-ca6f-433e-95b2-36744cb57d9d\', keyFileVariable: \'sshkey\', usernameVariable: \'user\')])'
      }
    }
    stage('deploy') {
      steps {
        sh 'scp -r * -p 22 root@10.108.23.122:/opt/ '
      }
    }
  }
  environment {
    pass = 'credentials(\'pass\')'
  }
}