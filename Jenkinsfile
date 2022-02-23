pipeline{

    agent any

// uncomment the following lines by removing /* and */ to enable
   tools{
       nodejs 'nodejs' 
    }
   

    stages{
        stage('compile'){
            steps{
                echo 'this is the compile job'
                sh 'npm install'
               }
        }
        stage('test'){
            steps{
                echo 'this is the test job'
                sh 'npm test'
                }
        }
        stage('package'){
            steps{
                echo 'this is the package job'
                sh 'npm run package'
                sleep 2
            }
        }
    }
    
    post{
        always{
            echo 'this pipeline as code..'
        }
        
    }
    
}
