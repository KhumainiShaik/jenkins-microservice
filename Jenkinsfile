pipeline{
    agent { 
        docker { image 'node:22.11.0-alpine3.20' }
    }
    stages{
        stage('Build'){
            steps {
                sh 'node --eval "console.log(process.platform,process.env.CI)"'
                echo "Build"
            }
        }
        stage('Test'){
            steps {
                echo "Test"
            }
        }
        stage('Integration Test'){
            steps {
                echo "Integration Test"
            }
        }
    }
    post{
        always{
            echo 'I am awesome. I run always'
        }
        success{
            echo 'I run when you are successfull'
        }
        failure{
            echo 'I run when you fail'
        }
    }
}
