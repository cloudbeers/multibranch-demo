#!groovy
// Loads: https://gist.github.com/jglick/b13b509bc236566c8829
standardBuild {
    environment = 'golang:1.5.0'
    mainScript = '''
go build -v helloworld.go
'''
    postScript = '''
ls -l
./helloworld
'''
}
