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
                    clone("https://github.com/kuldeepmindpath07/jenkins-demo.git","kuldeep")
                }
            }
        }
        stage("deploy"){
            steps{
                echo "this is deploying the code"
                sh "docker stop a96b5bf7ca7d2fdab36e6d6b980c82eb4803b9c891218e8002c948dd21f60dde"
                sh "docker-compose down && docker-compose up -d"    
            }
        }
    }
}
