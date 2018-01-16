pipeline {
node {
  ws("workspace/${env.JOB_NAME}/${env.BRANCH_NAME}".replace('%2F', '_')) {
    // Mark the code checkout 'stage'....
    stage 'Checkout'
    checkout scm

    // Mark the code build 'stage'....
    stage 'Build'

    def mvnHome = tool 'maven'

    sh "${mvnHome}/bin/mvn clean verify -B"
    
    junit testResults: '**/surefire-reports/*.xml'
  }
}
}
