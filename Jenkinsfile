pipeline{
	agent{
		label{
			label'built-in'
			customWorkspace'/data/project'
			}
		}
	stages{
		stage('new index.html'){
			steps{
			sh 'scp -i /root/sk2 /data/project/index.html ec2-user@15.206.27.55:/data/project/'
			}
		}
		stage('deploy on slave'){
			agent{
				label{
					lable 'slave'
				}
			}
			steps{
				sh 'sudo cp /data/project/index.html /var/www/html/'
			}
		}
	}
}
