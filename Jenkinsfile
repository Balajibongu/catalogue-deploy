pipeline{
    // agent any 
    agent{
        label "AGENT-1"
    }
    environment{
        name = "balaji"
    }
    options{
        timeout(time: 10, unit: 'MINUTES')
        disableConcurrentBuilds() 
        ansiColor('xterm')
    } 
    stages{
        stage("build"){
            steps{
                withAWS(credentials: 'aws-credentials', region: 'us-east-1')
                {
                    sh """
                        aws eks update-kubeconfig --region us-east-1 --name roboshop-dev
                        kubectl get nodes 
                    """
                }
            }
        }

    }

    post{
        always{
            echo "cleaning work space"
            cleanWs()
        }
        
    }
}