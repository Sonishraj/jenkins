pipeline {
    agent any
    tools {
        jdk 'JDK'
        maven 'MAVEN_HOME'
    }

    stages {
        stage('GitHub project pull') {
            steps {
                git branch: 'main', url: 'https://github.com/Sonishraj/jenkins.git'
            }
            
        }
        stage('mavenbuild'){
            steps {
                bat "mvn package -Dmaven.test.skip"
            }
        }
	stage('zip') {
		steps {
        		zip zipFile: 'target.zip', archive: false, dir: 'archive'
                	archiveArtifacts artifacts: 'target.zip', fingerprint: true
		}
   	}
    }
}
