#!/usr/bin/groovy

pipeline {
    agent any

    options {
        disableConcurrentBuilds()
    }

    stages {

        stage("Build") {
            steps { buildApp() }
		}
	}
}

// steps
def buildApp() {
	dir ('epragathi/' ) {
		def appImage = docker.build("epragathi/myapp:${BUILD_NUMBER}")
	}
}
