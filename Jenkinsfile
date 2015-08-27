#!groovy
stage 'checkout'
node {
  checkout scm
  stage 'build'
  docker.image('golang:1.5.0').inside {
    sh 'go build -v hello-world.go'
  }
  sh 'ls -l'
  sh './hello-world'
}
