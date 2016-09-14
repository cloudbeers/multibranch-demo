@Library('github.com/cloudbeers/multibranch-demo-lib@0037657b32b8e865cf99c4ed946577df95b65823') _
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
