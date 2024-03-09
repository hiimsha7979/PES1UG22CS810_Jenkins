 pipeline{
  agent any
  stages{
    stage('Clone repository'){
      steps{
        checkout([$class: 'GitSCM',
                branches: [[name: '*/main']],
                userRemoteConfigs: [[url: 'https://github.com/hiimsha7979/PES1UG22CS810_Jenkins.git']]
      ])
      }
    }
   
    stage('Deploy'){
      steps{
        echo 'deploy'
      }
    }
  }
  post {
    failure {
      error 'Pipeline failed'
    }
  }

  
} 
