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
				sh 'whoami'
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
				sh 'whoami'
				sh 'du -h'
			}
		}
        stage('5-s5'){
			parallel {
				stage('p1'){
					steps{
						echo "first parallel-stage"
					}
				}
				stage('p2'){
					steps{
						echo "second parallel-stage"
					}
				}
			}
        }
        stage('5-scriptdemo'){
            steps{
                sh 'bash -x /var/lib/jenkins/workspace/team6-demo1-pipeline/scriptdemo.sh'
            }
        }
	}
}
