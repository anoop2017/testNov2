pipeline {
    agent any
	stages 
	{
		stage('SCM Checkout') {

				steps {
					   git 'https://github.com/anoop2017/testNov2'
				}
			}
		stage('UNIT test'){
			steps {
			  "mvn deploy -P cloudhub-dev"
			}
		  }
		stage('Test') {
			steps {
				input('Do you want to proceed to deploy it to QA?')
			}
			}
		stage('Deploy QA'){
			steps {
			  "mvn deploy -P cloudhub-qa"
			}
		  }
		stage('Production') {
			steps {
				input('Do you want to proceed to deploy this to Prod?')
			}
			}
		stage('Deploy PROD')
		{
			steps {
			  "mvn deploy -P cloudhub-prod"
			}
		}
	}
}
