pipeline{
	agent any
	stages{
		stage('1-clonecode'){
			steps{
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'github-cred', url: 'https://github.com/etechteam6/team6-demo1.git']])
			}
		}
		stage('2-s2'){
			steps{
				sh 'lscpu'
				sh 'logname'
			}
		}
		stage('3-s3'){
			steps{
				sh 'df -h'
				sh 'touch team6'
			}
		}
		stage('4-s4'){
			steps{
				sh 'pwd'
				sh 'du -h'
			}
		}
	}
}