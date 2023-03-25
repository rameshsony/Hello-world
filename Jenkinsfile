pipeline {
    agent any
    

    stages {
        
        
        stage('Deployment') {
            steps {
                sshagent(['deployment-tomcat']) {
                   sh "scp -o StrictHostKeyChecking=no /var/lib/jenkins/workspace/build_job/webapp/target/webapp.war ec2-user@54.234.159.223:/opt/apache-tomcat-9.0.73/webapps"
}
                
            }
        }
        
    }
}
