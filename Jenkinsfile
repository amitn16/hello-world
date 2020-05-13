pipeline {
  agent docker
  stages {
    stage('1') {
      steps {
        echo 'Testing'
      }
    }

    stage('2') {
      agent any
      steps {
        container(name: 'docker', shell: 'sh') {
          sh '''ssh root@192.168.1.109
cd /root/myimages
docker start deploy10'''
        }

        echo 'completed'
      }
    }

  }
}
