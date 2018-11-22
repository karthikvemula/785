
node('master') 
{
    stage('ContinuousDownload-master') 
    {
       git 'https://github.com/selenium-saikrishna/maven.git'

    }
    stage('ContinuousBuild-master') 
    {
      sh 'mvn package'
    }
    stage('ContinuousDeployment-master')
    {
        sh 'scp /home/ubuntu/.jenkins/workspace/multi/webapp/target/webapp.war ubuntu@172.31.87.17:/var/lib/tomcat7/webapps/hai.war'
    }
    stage('Continuoustesting-master')
    {
        git 'https://github.com/selenium-saikrishna/FunctionalTesting.git'
    }
}

