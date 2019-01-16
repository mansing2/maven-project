pipeline
{
	agent any
	stages
		{
			stage ('build')
			{
				agent { label 'docker-slave' }
				steps{
					echo 'build'
				}
			}
			
			stage ('test')
			{
				steps{
					echo 'test'
				}
			}
		}
	
}
