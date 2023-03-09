pipeline {
    agent {
        dockerfile true
    }

    stages {
        stage('checkout') {
            steps {
               // echo 'Hello World'
               checkout scm 
            }
        }
        // stage('Build') {
        //     steps {
        //         sh ''' 
        //         docker build -t my-docker-gs-ping:v1.0 -f Dockerfile
        //         '''
        //     }
        // }

        stage('archive') {
             steps {
                archiveArtifacts(artifacts: '**/*', followSymlinks: false)
      }
    }

    }
}
