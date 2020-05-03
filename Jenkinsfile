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
		stage("Stopping the Grid"){
			steps{
				sh "docker-compose down"
			}
		}

	}
	

}