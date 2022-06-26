pipeline {
  agent any
  
  options {
    timestamps()
    timeout(time: 30, unit: 'MINUTES')
  }
  
  parameters {
    string(name: 'branch', defaultValue: 'master', description: '分支')
    string (name: 'version', defaultValue: '0.0.1', description: '版本')
  }
  
  stages{
    
    stage('获取代码') {
      steps {
        echo '获取代码'
      }
    }
    
  }
}
