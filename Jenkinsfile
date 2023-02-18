pipeline
{
    agent any
    stages
    {
        stage('Build')
        {
            steps
            {
                sh 'g++ -c PES1UG20CS587.cpp'
                sh 'g++ -o PES1UG20CS587 PES1UG20CS587.cpp'
                echo 'BUILD STAGE SUCCESSFUL'
            }
        }
        stage('Test')
        {
            steps
            {
                sh './PES1UG20CS'
                echo 'TEST STAGE SUCCESSFUL'
            }
        }
        stage('Deploy')
        {
            steps
            {
                echo 'DEPLOY STAGE SUCCESSFUL'
            }
        }
    }
    post
    {
        failure
        {
            echo 'PIPELINE FAILED'
        }
    }
}
