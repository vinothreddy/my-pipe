node('built-in') 
{
    stage('Continuous Download') 
	{
    git 'https://github.com/vinothreddy/my-pipe.git'
	}
    stage('Continuous Build') 
	{
    sh label: '', script: 'mvn package'
	}
   
    stage('Continuous Deployment') 
   
	 {
	
 sh label: '', script: 'scp  /home/ubuntu/.jenkins/workspace/multibranch_loans/webapp/target/webapp.war  ubuntu@172.31.21.16:/var/lib/tomcat8/webapps/qaenv.war'
	}
}
