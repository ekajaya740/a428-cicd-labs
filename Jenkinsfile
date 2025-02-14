node {
  def image
  stage('Pull Image'){
    image = docker.image('node:16-buster-slim')
    image.pull()
  }
  stage('Build'){
    image.inside('-p 3000:3000'){
      sh 'npm install'
    }
  }
}

