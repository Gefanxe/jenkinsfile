pipeline {
  agent any
  parameters {
    string(name: 'INPUT', defaultValue: 'test', description: '字串輸入')
    password(name: 'PASSWORD', defaultValue: '', description: '密碼輸入')
  }
  environment {
    MY_CREDS = credentials('nas-smb')
    
  }
  stages {
    stage('test') {
      steps {
        sh """
          # mkdir -p nas
          # mount -t smbfs "//WORKGROUP;${MY_CREDS}@192.168.88.233/Web" nas
          # cp nas/apidoc.json ./
          curl -X GET "http://192.168.88.166:3000/test?ps=${MY_CREDS}"
        """
      }
    }
  }

}