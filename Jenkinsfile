pipeline{
	agent any
	
	tools{
		maven 'maven'
		}
		
		stages{
			stage('checkout'){
				steps{
					git branch:'main',url:'https://github.com/DivyanshuChauhan03/revisionanisble'
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
					sh 'ansible-playbook ansible/playbook.yml -i ansible/hosts.ini'
					}
				}
			}
		}
		
		
