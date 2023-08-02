pipeline{

    agent any


    tools{
       nodejs 'nodejs 
    }
    

    stages{
        stage('build-the-app'){
            steps{
                echo 'this is the build job'
                sh 'npm install'
                
            }
        }
        stage('test-the-app'){
            steps{
                echo 'this is the test job'
                sh 'npm test'
                
            }
        }
        stage('package-the-app'){
            steps{
                echo 'this is the Package job'
                sh 'npm run package'
                
            }
        }
    }
    
    post{
        always{
            echo 'this pipeline has completed...'
        }
        
    }
    
}
