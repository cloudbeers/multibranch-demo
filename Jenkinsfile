#!groovy
stage 'checkout'
echo 'hello from master'
node {
  checkout scm
  stage 'run'
  sh 'ls -l'
}
