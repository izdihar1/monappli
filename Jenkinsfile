pipeline{
  agent any
  {tool name: 'D:\\apache-maven-3.8.3', type: 'maven'}
  stages{
    stage("Delete workspace"){
      steps{
        cleanWs deleteDirs:true
        checkout scm
      }
    }
    stage("Build monappli"){
        steps{
        bat ''' mvn clean install '''
        }
     }
  }
}
