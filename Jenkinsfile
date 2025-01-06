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
                git url: "https://github.com/kuldeepmindpath07/shared-variables.git", branch: "kuldeep"
            }
        }
        stage("deploy"){
            steps{
                echo "this is deploying the code"
                sh "docker-compose down && docker-compose up -d"    
            }
        }
    }
}
