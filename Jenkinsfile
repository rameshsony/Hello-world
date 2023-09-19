pipeline {
    agent any
    

    stages {
        
        
        stage('Deploy') {
            steps {
                sshagent(['tomcat-deployment']) {
                    sh "scp -o StrictHostKeyChecking=no /var/lib/jenkins/workspace/build_job/webapp/target/webapp.war ec2-user@54.164.208.239:/opt/apache-tomcat-9.0.80/webapps"
}
            }
        }
    }
}
