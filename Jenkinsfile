
pipeline {
  agent any
    stages {
      stage('Repository') {
        steps {
           echo "checkout scm"
        }
      }
      stage('Test & Build') {
        steps {
          sh "echo ${env.BUILD_NUMBER}"
          sh "echo ${env.WORKSPACE}"
          sh "touch archivo.txt"
          sh "mkdir -p micarpeta"
          sh "touch micarpeta/mifile.txt"
	  sh "python main.py"
        }
      }
      stage('Deploy') {
        steps {
          sh "ls -la"
          sh "ls -la micarpeta"
          sh 'echo deploy'
        }
      }
   }
}

