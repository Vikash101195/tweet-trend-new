pipeline {
agent {
    docker {
        image 'abhishekf5/maven-abhishek-docker-agent:v1'
        args '--user root -v /var/run/docker.sock:/var/run/docker.sock'
    }
}

stages {
    stage('Checkout'){
      steps{
      echo 'Checking out the code'
      git branch: 'main', url: 'https://github.com/Vikash101195/tweet-trend-new.git'
      }
    }
}
}
