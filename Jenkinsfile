pipeline{
  agent any
  tools {
    maven "maven3.8.6"
  }
 stages {
   stage('1GetCode'){
     steps{
       sh "echo 'cloning the first application' "
       git branch: 'development', credentialsId: 'gitHubCredentials', url: 'https://github.com/chinasaorji/maven-web-application'
     }
   }
   stage('2Test+Build'){
     steps{
       sh "echo 'running JUnit-test-cases'"
       sh "echo 'testing must pass to create artifacts'"
       sh "mvn clean package"
     }
   }
   /*
   stage('3CodeQuality'){
     steps{
       sh "echo 'running CodeQualityAnalysis'"
       sh "mvn sonar:sonar"
  }
}
   stage('4uploadNexus'){
     steps{
       sh "mvn deploy"
  }       
}
   //stage('5deploytouat'){}
   //stage('approval gate'){}
   stage('7deploytoprod'){
     steps{
       deploy adapters: [tomcat9(credentialsId: 'tomcat9', path: '', url: 'http://54.85.253.71:8080/')], contextPath: null, war: 'target/*war'     
     }  
  }
 }
 post{
   always{
     emailext body: '''Dear team,

Please check build status

Regards
Chinasa''', recipientProviders: [buildUser(), developers(), contributor()], subject: 'success', to: 'chinasa12_orji@yahoo.com'
  }
   success{
     emailext body: '''Dear team,

Look into this build and refer back

Regards
Chinasa''', recipientProviders: [buildUser(), developers(), contributor()], subject: 'success', to: 'chinasa12_orji@yahoo.com'
  }
   failure{
     emailext body: '''Dear team,

Look into this failed build please.

Regards
Chinasa''', recipientProviders: [buildUser(), developers(), contributor()], subject: 'success', to: 'chinasa12_orji@yahoo.com'
    }
  }    
  */
} 
}
