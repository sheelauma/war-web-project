pipeline {
    agent any

    stages {
        stage('continuous download') {
            steps {
            git 'https://github.com/koddas/war-web-project.git'    
            }
        }
         stage('continuous build') {
            steps {
             sh 'mvn install'   
            }
        }
         stage('continuous deploy') {
            steps {
            sh 'scp target/wwp-1.0.0.war uma@172.17.0.2:/opt/apache-tomcat-9.0.56/webapps'   
            }
        }
    }
}
