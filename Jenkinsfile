node {
  def image
  stage('Checkout') {
    steps {
      checkout scm
    }
  }
  stage('Pull Image'){
    image = docker.image('node:16-buster-slim')
    image.pull()
  }
  stage('Build'){
    image.inside('-p 3000:3000'){
      sh 'npm install'
    }
  }
  stage("Test"){
    image.inside('-p 3000:3000'){
      sh './jenkins/scripts/test.sh'
    }
  }
}


