pipeline{
    agent any

        stages{
            stage(TEST1){
                steps{
                    echo 'Test1'
                }
            }

            stage(TEST2){
                steps{
                    echo 'Test2'
                    emailext body: 'TEST', subject: 'TEST', to: 'gupta@local.com'
                }
            }
        }

    post{
        fixed{
            echo "Hello"
        }
        failure{
            echo "Failed State"
            emailext body: 'TEST', subject: 'TEST', to: 'gupta@local.com'
        }
        cleanup{
            echo "Common steps"
        }
    }
}
