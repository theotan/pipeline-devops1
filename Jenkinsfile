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
		stage('mid') {
			steps {
			echo "The mid stage is happening"
			sleep 20
			}
		}
		stage('compile-fizz') {
			steps {
			sh 'go build fizzbuzz.go'
			}
		}
    }
    post {
		always {
			archiveArtifacts artifacts: 'synonyms', fingerprint: true
		}
    }
}
