pipeline{
	agent any
	stages{
		stage("starts Grid"){
		steps{
			sh "docker-compose up -d hub chrome firefox"
			}
		}
		stage("Run Test"){
			steps{
				sh "docker-compose up search-module book-flight-module"
			}
		}
		
	}
	post{
		always{
			archiveArtfacts artifacts: 'output/**'
			sh "docker-compose down"
		}
	}
	

}