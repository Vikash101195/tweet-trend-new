pipeline {
agent {
    node {
        label 'maven'
    }
}

stages {
    stage('Checkout'){
      steps{
      echo 'Checking out the code'
      // git branch: 'main', url: 'https://github.com/Vikash101195/tweet-trend-new.git'
      }
    }

    stage('Maven Build'){
        steps{
        sh 'mvn clean deploy'
        }
    }

    stage('Sonar quality check'){
        environment{
            scannerHome = tool 'vikky-sonar-scanner'
        }
        steps{
             
             withSonarQubeEnv('vikky-sonarqube-server') // If you have configured more than one global server connection, you can specify its name
             sh "${scannerHome}/bin/sonar-scanner"
        }
    }
}
}
