pipeline{
	agent any
	stages{
		stage('1-s1'){
			steps{
				sh 'cat /etc/passwd'
				sh 'whoami'
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