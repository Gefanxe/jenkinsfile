pipeline {
  agent any
  parameters {
    string(name: 'INPUT', defaultValue: 'test', description: '字串輸入')
    password(name: 'PASSWORD', defaultValue: '', description: '密碼輸入')
  }
  environment {
    MY_CREDS = credentials('nas-smb')
    MY_CREDS_USR = "${params.INPUT}"
    MY_CREDS_PSW = "${params.PASSWORD}"
  }
  stages {
    stage('test') {
      steps {
        sh """
          echo "credentials: ${MY_CREDS}"
          
          echo "ID: ${MY_CREDS_USR}"
          echo "PW: ${MY_CREDS_PSW}"
        """
      }
    }
  }

}