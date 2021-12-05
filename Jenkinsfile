def imageName = 'luiszavaleta/movies-loader'

node{
    stage('Checkout'){
        checkout scm
    }
    stage('Unit Tests'){
        sh "docker build -t ${imageName}-test -f Dockerfile.test ."
        sh "docker run --rm ${imageName}-test"
    }

    stage('Unit Tests DLS'){
        def imageTest= docker.build("${imageName}-test", "-f Dockerfile.test .")
        imageTest.inside{
            sh 'python test_main.py'
        }
        sh "docker run --rm -v $PWD/reports:/app/reports ${imageName}-test"
        junit "$PWD/reports/*.xml"
    }
}
