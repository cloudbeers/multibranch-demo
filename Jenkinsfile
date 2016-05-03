// Loads: https://github.com/jenkinsci/github-branch-source-plugin/blob/master/demo/workflow-libs/vars/standardBuild.groovy
standardBuild {
    environment = 'golang:1.5.0'
    mainScript = '''
go version
go build -v hello-world.go
'''
    postScript = '''
ls -l
./hello-world
'''
}
