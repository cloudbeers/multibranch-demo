#!groovy
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
