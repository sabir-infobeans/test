pipeline {
   agent any
   stages {
       stage('Build Code') {
           steps {
               powershell '''
               echo "Building Artifact"
               '''
           }
       }
      stage('Deploy Code') {
          steps {
               powershell """
               echo "Deploying Code"
               """
          }
      }
   }
}
