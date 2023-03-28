node {
        def app
        stage('Clone repository') {
                checkout scm
        }
        stage('Build image') {
          app=docker.build("filipbosilkov/devops4")
        }
	stage('Push image') {
    	docker.withRegistry('https://registry.hub.docker.com', 'docker') {
                        dockerImage.push()
    }
  }
}
