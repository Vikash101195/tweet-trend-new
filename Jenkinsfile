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
}
}
