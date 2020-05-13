pipeline {
  agent any
  stages {
    stage('1') {
      steps {
        echo 'Testing'
      }
    }

    stage('') {
      steps {
        container(name: 'docker', shell: 'sh') {
          sh '''ssh root@192.168.1.109
cd /root/myimages
docker start deploy10'''
        }

      }
    }

  }
}