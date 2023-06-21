pipeline{

    agent any

// uncomment the following lines by removing /* and */ to enable
    tools{
       nodejs 'nodejs' 
    }    

    stages{
        stage('build'){
            steps{
                echo 'this is the first build app'
                sh 'npm install'
                
            }
        }
        stage('test'){
            steps{
                echo 'this is to test the app'
                sh 'npm test'
                
            }
        }
        stage('package'){
            steps{
                echo 'this is to package the app'
                sh 'npm run package'
               
            }
        }
    }
    
    post{
        always{
            echo 'this is my first pipeline ...'
        }
        
    }
    
}
