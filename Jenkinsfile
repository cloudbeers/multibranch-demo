#!groovy
// Loads: https://gist.github.com/jglick/b13b509bc236566c8829
standardBuild {
    environment = 'golang:1.4.0'
    mainScript = '''
go version
go build -v hello-world.go
'''
    postScript = '''
ls -l
./hello-world
'''
}
