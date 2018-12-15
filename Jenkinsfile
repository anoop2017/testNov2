node {
  
  stage('SCM Checkout')
  {
    git 'https://github.com/anoop2017/testNov2'
  }
  stage('UNIT test'){
    def mvnHome = tool name: 'D:\\Mule\\Maven\\apache-maven-3.5.4-bin\\apache-maven-3.5.4', type: 'maven'
    def mavenHome = 'D:\\Mule\\Maven\\apache-maven-3.5.4-bin\\apache-maven-3.5.4'
   "${mvnHome}/bin/mvn deploy -P cloudhub-dev"
  }
  stage('Test') {
	steps {
		input('Do you want to proceed to deploy it to QA?')
	}
	}
	stage('Deploy QA'){
    def mvnHome = tool name: 'D:\\Mule\\Maven\\apache-maven-3.5.4-bin\\apache-maven-3.5.4', type: 'maven'
    def mavenHome = 'D:\\Mule\\Maven\\apache-maven-3.5.4-bin\\apache-maven-3.5.4'
    steps {
      "${mvnHome}/bin/mvn deploy -P cloudhub-qa"
    }
  }
    stage('Production') {
	steps {
		input('Do you want to proceed to deploy this to Prod?')
	}
	}
	stage('Deploy PROD'){
    def mvnHome = tool name: 'D:\\Mule\\Maven\\apache-maven-3.5.4-bin\\apache-maven-3.5.4', type: 'maven'
    def mavenHome = 'D:\\Mule\\Maven\\apache-maven-3.5.4-bin\\apache-maven-3.5.4'
    steps {
      "${mvnHome}/bin/mvn deploy -P cloudhub-prod"
    }
  }
  

}
