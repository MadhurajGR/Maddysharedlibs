@Library("maddylibs") _
pipeline{
    agent any
    stages{
        stage("maven build"){
            steps{
              sh 'mvn clean package -DskipTests=true'
            }
        }
        stage(" Dev Tomcat Deploy"){
            steps{
                tomcatDeploy("172.31.32.87","ec2-user","tomcat-dev")
                }   
            }
        }
    }
