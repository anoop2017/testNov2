node {  
	stage('SCM Checkout')
	  {
	    git 'https://github.com/anoop2017/testNov2'
	  }
	stage('UNIT test'){
	    def mvnHome = tool name: 'D:\\Mule\\Maven\\apache-maven-3.5.4-bin\\apache-maven-3.5.4', type: 'maven'
	    def mavenHome = 'D:\\Mule\\Maven\\apache-maven-3.5.4-bin\\apache-maven-3.5.4'
	    sh "mvn deploy -P cloudhub-dev"
		//def mvn_version = 'M3'
		//withEnv( ["PATH+MAVEN=${tool mvn_version}/bin"] ) {

		
	  }
 }
