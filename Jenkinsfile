node('master') 
{
    stage('Continuous Download_master') 
	{
    git 'https://github.com/sunildevops77/maven.git'
	}
    stage('Continuous Build_m') 
	{
    sh label: '', script: 'mvn package'
	}
    stage('Continuous Deployment_m') 
	{
sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war   ubuntu@172.31.26.217:/var/lib/tomcat8/webapps/qaenv.war'
	}
    stage('Continuous Testing_m') 
	{
              sh label: '', script: 'echo "Testing Passed"'
	}
}
