pipeline {
  /* A declarative Pipeline */
    agent any

    stages {
        stage('Build') {
            steps {
                bat 'mvn --version'
                bat 'mvn clean package'
            }
            post{
              success{
                 echo 'Now Archiving....'
                 archiveArtifacts artifacts: '**/target/*.war'
              }
            }
        }
     }
}