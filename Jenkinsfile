pipeline {

    agent any

    tools {
        maven 'maven'
    }

    stages {

        stage('Git Pull') {
            steps {
                git branch: 'main',
                url: 'YOUR_GITHUB_REPO_LINK'
            }
        }

        stage('Build WAR') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Deploy to Tomcat') {
            steps {
                sh 'cp target/*.war /opt/tomcat/webapps/'
            }
        }

    }

}
