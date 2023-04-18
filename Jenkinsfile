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
          mail to: 'phirastor@proton.me', 
          subject: 'Test',
          body: 'Bonjour, ceci est un test',
          mimeType: 'text/html';
          slackSend botUSer: true, 
            channel: "exo", 
            message: "Jenkins build complete",
            tokenCredentialId: "slack-token";
        }
  }
}
  
