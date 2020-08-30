pipeline {
    agent any 
    stages {
        stage("Build") {
            steps {
                sh "mvn clean package"
            }
        }
        
        stage("Deploy") {
            steps {
                deploy adapters: [tomcat7(credentialsId: 'c094365d-b1ec-46eb-83db-671e2a3cbffe', path: '', url: 'http://3.17.24.33:8080/')], contextPath: 'java-web-app', war: '**/java-web-project.war'
            }
        }
    }
}
