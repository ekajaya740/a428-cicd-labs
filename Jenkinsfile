node {
  stage('Build'){
    docker.image('node:16-buster-slim').pull().inside('-p 3000:3000'){
      sh 'npm install'
    }
  }
}
