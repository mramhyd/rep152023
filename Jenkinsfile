node('built-in') 
{
    stage('Continuous Download_master') 
	{
    git 'https://github.com/mramhyd/rep152023.git'
	}
    stage('Continuous Build_master') 
	{
            sh label: '', script: 'mvn package'
	}

    stage('Continuous Deployment') 
	{
           sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/firstjob_loans/webapp/target/webapp.war   ubuntu@172.31.39.206:/var/lib/tomcat9/webapps/qaenv.war'
	}

}
