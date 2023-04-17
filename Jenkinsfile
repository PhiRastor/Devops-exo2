pipeline {
  agent any
  triggers {
    pollSCM('H/2 * * * *')
  }
  
  stages {
    stage('HelloWorld') {
      steps {
        echo 'Hello world!!!!?'
      }
    }
  }
  post {
        always {
          to: 'phirastor@proton.me', 
          subject: 'Test',
          body: 'Bonjour, ceci est un test',
          mimeType: 'text/html'
        }
  }
}
  
