pipeline {
    agent any
    stages {
        stage ('Compile Stage') {

            steps {
                def mvnHome = tool 'maven'
                sh "${mvnHome}/bin/mvn clean compile"
                }
            }

        stage ('Testing Stage') {

            steps {
                def mvnHome = tool 'maven'
                sh "${mvnHome}/bin/mvn test"
                }
            }
        }
 }
