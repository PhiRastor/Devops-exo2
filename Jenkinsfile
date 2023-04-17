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
            emailext body: 'A Test EMail', recipientProviders: [[$class: 'DevelopersRecipientProvider'], [$class: 'RequesterRecipientProvider']], subject: 'Test'
        }
  }
}
  
