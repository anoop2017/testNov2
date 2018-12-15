node {
  
  stage('SCM Checkout')
  {
    git 'https://github.com/anoop2017/testNov2'
  }
  stage('UNIT test'){
    def mvnHome = tool name: 'D:\\Mule\\Maven\\apache-maven-3.5.4-bin\\apache-maven-3.5.4', type: 'maven'
    echo 'this is my unit testing'
    sh "${mvnHome}/bin/mvn package"
  }

}
