
node('master') 
{
    stage('ContinuousDownload-loan') 
    {
       git 'https://github.com/selenium-saikrishna/maven.git'
    }
    stage('ContinuousBuild-loan') 
    {
      sh 'mvn package'
    }
    stage('ContinuousDeployment-loan')
    {
        sh 'scp /home/ubuntu/.jenkins/workspace/multi/webapp/target/webapp.war ubuntu@172.31.87.17:/var/lib/tomcat7/webapps/hai.war'
    }
    stage('Continuoustesting-loan')
    {
        git 'https://github.com/selenium-saikrishna/FunctionalTesting.git'
    }
}

