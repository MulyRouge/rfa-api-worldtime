pipeline {
  agent any
   tools{
     maven '3.8.6'
     nodejs 'Nodejs_for_newman'
    
     }
  stages {
    stage('Build Application "no Aço como André Dionisio"') { 
      steps {
        sh 'mvn clean install'
      }
     } 
  
   stage('Test Integration Application') { 
      steps {
       
       sh 'newman run  /var/jenkins_home/workspace/worldtimezone-CI-pipeline/src/test/integration/Worldtimezone_tes.postman_collection.json'
      }
    }
   } 
}
