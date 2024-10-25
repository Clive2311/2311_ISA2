pipeline {
	agent any
	
	stages {
		stage('Build Docker image') {
			steps {
				script {
					bat "docker build -t clive2311/2311_MDP_ISA2 ."
				}
			}
		}
		
		stage('Delete Container if already exists') {
			steps {
				script {
					bat "docker rm -f 2311 || exit 0"
				}
			}
		}
		
		stage('Run container') {
			steps {
				script {
					bat "docker run -d --name 2311 -t clive2311/2311_MDP_ISA2"
				}
			}
		}
	}
}
