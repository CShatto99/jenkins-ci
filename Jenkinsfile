#!/usr/bin/env groovy

pipeline {
	agent any
	stages {
		stage('Build') {
			steps {
				echo 'Building application...'
			}
		}
		stage('Test') {
			steps {
				sh 'false'
			}
		}
		stage('Deploy') {
			when {
				expression {
					currentBuild.result == null || currentBuild.result == 'SUCCESS'
				}
			}
			steps {
				echo 'Deploying application...'
			}
		}
	}
}