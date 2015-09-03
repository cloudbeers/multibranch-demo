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
            sh 'echo ran branch a'
            input 'really?'
        }
    }
}, b: {
    node {
        sh 'sleep 5 && echo ran branch b'
    }
}
