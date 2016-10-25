@Library('github.com/cloudbeers/multibranch-demo-lib') _
properties([parameters([string(name: 'goVersion', defaultValue: '1.5.0', description: 'Which version of Go language to use.')])])
def image = "golang:${params.goVersion}"
standardBuild {
    environment = image
    mainScript = '''
go version
go build -v hello-world.go
'''
    postScript = '''
ls -l
./hello-world
'''
}
