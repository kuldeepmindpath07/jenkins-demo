@Library('Shared')_
pipeline{
    agent any
    stages{
        stage("hello"){
            steps{
                script{
                    echo "shared variables done"
                    hello()
                }
            }
        }
        stage("code"){
            steps{
                script{
                
                    clone("https://github.com/kuldeepmindpath07/shared-variables.git", "kuldeep")
                }
            }
        }
        stage("deploy"){
            steps{
                echo "this is deployingfffffffffffffffff the code"
                sh "docker-compose up -d --remove-orphans"    
            }
        }
    }
}
