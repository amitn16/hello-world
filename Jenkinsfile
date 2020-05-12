pipeline {
	node ('192.168.1.109') {
		docker.withServer('tcp://192.168.1.109:2375') {
			image = docker.image('amitn16/deployansible').pull()
	}
}

	docker.withServer('tcp://192.168.1.109:2375','amit')

	docker.withServer("unix:///var/run/docker.sock"){
		myImage = docker.image("amitn16/deployansible")
		myImage.pull()
	}
    stages {
        stage('Build') { 
            steps {
                sh 'echo test' 
            }
        }
    }
}
