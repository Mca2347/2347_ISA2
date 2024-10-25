pipeline{
  agent any

  stages{
    stage('build docker image'){
      steps{
        script{
                //build Dockerfile into an image
                bat "docker build -t xacuti01/dock."
              }
            }
    }
    stage('build and run docker container'){
      steps{
        script{
                //remove the docker container with similar name to avoid conflicts
                bat "docker rm -f 2347 || exit0"
                bat "docker run -d --name 2347 xacuti01/dock"
              }
            }
    }
}
}  
  
