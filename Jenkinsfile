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
	
 sh label: '', script: 'scp  /home/ubuntu/.jenkins/workspace/multibranch_loans/webapp/target/webapp.war  ubuntu@172.31.39.219:/var/lib/tomcat9/webapps/qaenv.war'
	}
}
