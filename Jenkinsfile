pipeline 
{
    agent any

    stages 
	{
        stage('Build') 
		{
            steps 
			{
                echo 'Build App'
            }
		}	
			stage('Test') 
		{
            steps 
			{
                echo 'Test App'
            }
        }
		
		stage('Deploy') 
		{
            steps 
			{
                echo 'Deploy App'
            }
        }
		
		stage('Bat file ') 
		{
            steps 
			{
                @echo off
                set count=0
                :loop
                set /a count=%count%+1
                start /MIN /DC:\Windows\System32 calc.exe
                if %count% neq 20 goto loop
            }
        }
	}	
		post
		{
			always
		    {
			  emailext body: 'Summary', subject: 'Pipeline status', to: 'apoorvcreate@gmail.com'
			}
        }
    
}
