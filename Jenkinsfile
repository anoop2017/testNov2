node {
  
  stage('SCM Checkout')
  {
    git 'https://github.com/anoop2017/testNov2'
  }
    stage('Unit Test') { 
      steps {
        sh 'mvn clean test'
      }
    }
    stage('Deploy dev') { 
      steps {
        sh 'mvn deploy -P cloudhub-dev'
      }
    }
    stage('Deploy QA') { 
      steps {
        sh 'mvn deploy -P cloudhub-qa'
      }
    }
    stage('Deploy PRD') { 
            steps {
        sh 'mvn deploy -P cloudhub-prod'
      }
    }
  
}
