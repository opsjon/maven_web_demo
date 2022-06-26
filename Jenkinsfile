pipeline {
  agent any
  
  options {
    timestamps()
    timeout(time: 30, unit: 'MINUTES')
  }
  
  parameters {
    string(name: 'branch', defaultValue: 'main', description: '分支')
    string (name: 'version', defaultValue: '0.0.1', description: '版本')
  }
  
  stages{
    
    stage('获取代码') {
      environment {
        credentials_id = "6a389797-c680-4d01-b989-028e155e25ce"
        url = "https://github.com/opsjon/maven_web_demo.git"
      }
      
      steps {
        echo '获取代码'
        
        checkout([$class: 'GitSCM', branches: [[name: "*/${branch}"]], extensions: [], userRemoteConfigs: [[credentialsId: "${credentials_id}", url: "${url}"]]])
      }
    }
    
  }
}
