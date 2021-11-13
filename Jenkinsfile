def imageName = 'mlabouardy/movies-loader'

node{
    stage('Checkout'){
        checkout scm
    }
    stage('unit test'){
        def imageTest= docker.build("${imageName}-test",  "-f Dockerfile.test .")
        imageTest.inside{
            sh 'python test_main.py'
        }
    }
}