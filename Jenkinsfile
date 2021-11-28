pipeline {
    agent any
    tools {
	go 'Golang version 17.3'
    }
    stages {
	stage('compilation') {
	    steps {
		sh 'go build synonyms.go'
	    }
	}
	stage('trial-run') {
	    steps {
		sh './synonyms'
	    }
	}
    }
    post {
	always {
	    archiveArtifacts artifacts: 'synonyms', fingerprint: true
	}
    }
}
