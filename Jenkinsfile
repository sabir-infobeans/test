pipeline {
   agent any
   stages {
       stage('Build Code') {
           steps {
               powershell """
               echo "Building Artifact from Develop Branch"
               """
           }
       }
      stage('Deploy Code') {
          steps {
               powershell """
               echo "Deploying Code from Develop Branch"
               """
          }
      }
   }
}
