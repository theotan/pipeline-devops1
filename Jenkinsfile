pipeline {
    agent any
    tools {
	go 'Golang version 17.3'
    }
    stages {
	stage('compilation') {
	    steps {
		sh 'go build fizzbuzz.go'
	    }
	}
	stage('trial-run') {
	    steps {
		sh './fizzbuzz'
	    }
	}
    }
    post {
	always {
	    archiveArtifacts artifacts: 'synonyms', fingerprint: true
	}
    }
}
