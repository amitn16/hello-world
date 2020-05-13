pipeline {
	agent {
		withDockerServer([uri: 'tcp://192.168.1.109:2375']) {
				image = docker.image('amitn16/deployansible').pull()
		}
	}
}

	withDockerServer([uri: 'tcp://192.168.1.109:2375'],'amitn16')

	withDockerServer("unix:///var/run/docker.sock"){
		myImage = docker.image("amitn16/deployansible")
		myImage.pull()
	}
    stages {
        stage('Build') { 
            steps {
                eacho 'Test1' 
            }
        }
    stage('Test') {
            steps {
                echo 'test2'
            }
        }
    stage('Deliver') { 
            steps {
                sh 'Test 3' 
            }    
        }
    }
