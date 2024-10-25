pipeline {
	agent any {
	
	stages {
		stage('Clone repository') {
			steps {
				script {
					bat "git clone https://github.com/Clive2311/2311_ISA2.git"
				}
			}
		}
	
		stage('Build Docker image') {
			steps {
				script {
					bat "docker build -t Clive2311/2311_MDP_ISA2 ."
				}
			}
		}
		
		stage('Delete Container') {
			steps {
				script {
					bat "docker rm -f 2311 || exit 0"
				}
			}
		}
		
		stage('Run container') {
			steps {
				script {
					bat "docker run -d --name 2311 -t Clive2311/2311_MDP_ISA2"
				}
			}
		}
	}
}
