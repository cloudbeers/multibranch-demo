@Library('github.com/cloudbeers/multibranch-demo-lib') _
standardBuild {
    environment = 'golang:1.5.0'
    mainScript = '''
go version
'''
    postScript = '''
ls -l
exit 1
'''
}
