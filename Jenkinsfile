pipeline {
  agent any
   tools{
     maven '3.8.6'
     }
  stages {
    stage('Build Application "no Aço como André Dionisio"') { 
      steps {
        sh 'mvn clean install'
      }
     }
    }
   stages {
    stage('Deploy Application "no Aço"') { 
      steps {
        sh 'clean package deploy -DmuleDeploy'
      }
    }
  }
}
