@Library('github.com/cloudbeers/multibranch-demo-lib') _
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
parallel a: {
    node {
        retry(5) {
            sh 'echo ran branch a'
            input 'really?'
        }
    }
}, b: {
    node {
        sh 'sleep 5 && echo ran branch b'
    }
}
