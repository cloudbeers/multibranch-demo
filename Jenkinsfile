@Library('github.com/cloudbeers/multibranch-demo-lib@0037657') _
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
