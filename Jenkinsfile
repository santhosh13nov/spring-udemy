pipeline {
    agent {
        label "master"
    }
    tools {
        // Note: this should match with the tool name configured in your jenkins instance (JENKINS_URL/configureTools/)
        maven "maven"
        jdk "jdk8"
    }
 
    stages {
        stage("clone code") {
            steps {
                script {
                    // Let's clone the source
                    git 'git@github.com:santhosh13nov/spring-udemy.git';
                }
            }
        }
        stage("mvn build") {
            steps {
                script {
                    // If you are using Windows then you should use "bat" step
                    // Since unit testing is out of the scope we skip them
                   sh 'mvn clean package'
                }
            }
        }
        
    }
}
