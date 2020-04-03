pipeline {
  agent any
  parameters {
    string(name: 'INPUT', defaultValue: 'test', description: '字串輸入')
    password(name: 'PASSWORD', defaultValue: '', description: '密碼輸入')
  }
  environment {
    test = 'var'
  }
  stages {
    stage('test') {
      steps {
        sh """
          echo "$INPUT"

          echo "$PASSWORD"
        """
      }
    }
  }

}