pipeline    
{
    agent any

    stages
    {
        stage('Install Dependencies')
        {
            steps
            {
                bat 'npm install'
            }
        }
        stage('Testing')
       {parallel
            {
                stage('Run Linting')
                {
                    steps
                    {
                        bat 'npm run lint'
                    }
                }
               
                stage('Unit Tests')
                {
                    steps
                    {
                        bat 'npm run test:unit'
                    }
                }
                
            }
        }
    }
}