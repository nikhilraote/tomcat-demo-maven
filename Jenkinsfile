pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Code already checked out'
            }
        }

        stage('Build WAR') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Deploy to Tomcat') {
            steps {
                sh '''
                cp target/tomcat-demo-app.war /opt/tomcat/webapps/
                '''
            }
        }
    }
}
