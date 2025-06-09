pipeline{
	agent again
	tools{
		maven'Maven'
	}
	stages{
		stage('Checkout'){
			steps{
				git bash:'master',url:'https://github.com/SUSHMITHA96-87/maven262.git'
			}
		}
		stage('Build'){
			steps{
				sh'mvn clean package'
			}
		}
		stage('Test'){
			steps{
				sh'mvn test'
			}
		}
		stage('Run Application'){
			steps{
				sh'java -jar target/Maven262-1.0-SNAPSHOT.jar'
			}
		}
	}
	post{
		success{
			echo'build and deploy successfully!'
		}
		failure{
			echo'build failure'
		}
	}
}
