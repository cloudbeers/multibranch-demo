#!groovy
// Loads: https://gist.github.com/jglick/b13b509bc236566c8829
standardBuild {
    environment = 'golang:1.5.0'
    mainScript = '''
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
            sh 'sleep 5 && echo ran branch a'
        }
    }
}, b: {
    node {
        sh 'sleep 10 && echo ran branch b'
    }
}
