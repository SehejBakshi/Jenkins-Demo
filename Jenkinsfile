﻿def builtDockerImage
	pipeline{
		agent any
		stages {
			stage('Clone repo') {
				steps {
					git url: 'https://github.com/SehejBakshi/Jenkins-Demo.git',branch: 'master'
				}
			}
			stage('Build image') {
				steps {
					script {
						builtDockerImage = docker.build "sehejbakshi/jenkins-project:v1.0"
					}
				}
			}   
			stage('Push image') {
				steps {
					script {
						docker.withRegistry('', 'aeaa9a2f-6b97-44ae-900f-76beed16d64b') {
							builtDockerImage.push()
						}
					}
				}
			}
		}
	}
}
}
}
}
}
}

