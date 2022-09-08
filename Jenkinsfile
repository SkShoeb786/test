pipeline{
	agent{
	label{
		label "built-in"
		customWorkspace '/mnt/git-repo'
	}
	}
	stages{
		stage("cloning git repo"){
			steps{
				echo "this is my 1st pipeline script from SCM"
			}
		}
	}
}
