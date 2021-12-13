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
    }

    stage('Test pararell execution'){
        parallel(
                'Hello': {
                    print 'Hello'
                },
                'World': {
                    print 'World'
                },
                'Luis': {
                    print 'Luis'
                },
                'Zavaleta': {
                    print 'Zavaleta'
                }

        )
    }

    
    stage('Build'){
        docker.build(imageName)
    }
}
