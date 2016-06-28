// Loads: https://github.com/jenkinsci/github-branch-source-plugin/blob/master/demo/workflow-libs/vars/standardBuild.groovy
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
