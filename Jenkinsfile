stage('library') {
    library 'github.com/cloudbeers/multibranch-demo-lib'
}
properties([parameters([string(name: 'goVersion', defaultValue: '1.5.0', description: 'Which version of Go language to use.')])])
standardBuild environment: "golang:${params.goVersion}",
    mainScript: '''
go version
go build -v hello-world.go
''',
    postScript: '''
ls -l
./hello-world
'''
