pipeline {
  agent any
    
  tools {nodejs "nodejs"}
    
  stages {
        
    stage('Build') {
      steps {
        sh """
        docker build -t dipendrac3/nodejs-pipeline-01 -f Dockerfile .
        docker push dipendrac3/nodejs-pipeline-01
        docker run -p 3032:9005 -d --name node-js-pipeline dipendrac3/nodejs-pipeline-01:latest
        """
      }
    }  
    
  }
}
