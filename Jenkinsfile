pipeline
{
	agent any
		stages{
				 stage('Building...'){
					 steps{
					 powershell 'dotnet build NewWebApi.sln -p:configuration=release -v:n'
					 echo "Building"
					 }
				
				
				 }

				 stage('Testing'){
					steps{
						powershell 'dotnet test'
						echo "Testing"
					}
				 }

				  stage('Publishing'){
					steps{
						powershell 'dotnet publish'
						echo "Publishing"
					}
				 }

        }

		post{
			always{
				archiveArtifacts '**'
			}
		}
}
