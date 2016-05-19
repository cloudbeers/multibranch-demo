// Loads: https://github.com/jenkinsci/github-branch-source-plugin/blob/master/demo/workflow-libs/vars/standardBuild.groovy
//standardBuild {
    environment = 'golang:1.5.0'
//    mainScript = '''
//go version
//go build -v hello-world.go
'''
//    postScript = '''
//ls -l
//./hello-world
//'''
//}

node {
   // Mark the code checkout 'stage'....
   stage 'Checkout'

   // Get some code from a GitHub repository
   git url: 'https://github.com/jglick/simple-maven-project-with-tests.git'

   // Get the maven tool.
   // ** NOTE: This 'M3' maven tool must be configured
   // **       in the global configuration.           
   def mvnHome = tool 'M3'

   // Mark the code build 'stage'....
   stage 'Build'
   // Run the maven build
   sh "${mvnHome}/bin/mvn install  -Dmaven.test.failure.ignore=true"
   step([$class: 'ArtifactArchiver', artifacts: '**/target/*.jar', fingerprint: true])
}
