pipeline {
  agent any
  stages {
    stage('Git CheckOut') {
      steps {
        git(url: 'https://github.com/adityasannidhi/BlueOcean_Pipeline.git', branch: 'main')
        echo 'Succesfully Checkedout from Github'
      }
    }

    stage('Compile') {
      steps {
        sh 'bash Compile.sh'
        echo 'Compiled Successfully!!'
      }
    }

    stage('Package') {
      steps {
        sh 'bash Package.sh'
        echo 'Packaged Successfully'
      }
    }

    stage('Deploy') {
      steps {
        sh 'bash Deploy.sh'
        echo 'Deployed!!'
      }
    }

  }
}