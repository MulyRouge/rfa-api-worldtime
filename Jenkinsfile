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
   stage('Deploy Application "no Aço"') { 
      steps {
        sh ' mvn clean package deploy -DmuleDeploy'
      }
    }
   stage('Test Integration Application') { 
      steps {
       nodejs(nodeJSInstallationName: 'Nodejs_for_newman')
       sh 'newman run  /var/jenkins_home/workspace/worldtimezone-CI-pipeline/src/test/integration/Worldtimezone_tes.postman_collection.json'
      }
    }
   } 
}
