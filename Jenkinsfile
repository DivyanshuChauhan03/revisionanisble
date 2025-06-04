pipeline{
	agent any
	
	tools{
		maven 'maven'
		}
		
		stages{
			stage('checkout'){
				steps{
					git branch:'main',url:''
					}
				}
			stage('build'){
				steps{
					sh 'mvn clean install'
					}
				}
			stage('Deploy'){
				steps{
					sh 'mvn clean package'
					sh 'ansible-playbook anisble/playbook.yml -i anisble/hosts.ini'
					}
				}
			}
		}
		
		
