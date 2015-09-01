#!groovy
standardBuild {
    environment = 'golang:1.4.2'
    mainScript = '''
go build -v hello-world.go
'''
    postScript = '''
ls -l
./hello-world
'''
}
