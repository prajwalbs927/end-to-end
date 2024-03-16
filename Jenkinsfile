pipeline{
  agent {label 'praju'}
  tools {
    jdk 'Java11'
    maven 'Maven3'
  }
  stages {
    stage ('Clean up workspace' ) {
      steps {
      cleanWs()
      }
      }
stage ('Check out from SCM') {
steps {
  git branch: 'main', credentialsID: 'github', url: 'https://github.com/prajwalbs927/end-to-end.git'
    }
}  
stage ('Build Application') {
  steps {
    sh "mvn clean package"
  }
}
    stage ('Test Application') {
      steps {
        sh "mvn test"
      }
    }
    
  } 
}
