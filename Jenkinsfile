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
			sh 'scp -i /root/sk2.pem /data/project/index.html ec2-user@15.206.27.55:/data/project'
			}
		}
		stage('deploy on slave'){
			agent{
				label{
					label'slave'
				}
			}
			steps{
				sh 'sudo cp /data/project/index.html /var/www/html/'
				sh 'sudo systemctl restart httpd'
			}
		}
	}
}
