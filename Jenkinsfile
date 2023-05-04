pipeline
{
    agent { label 'master'}
    enviroment
    {
        appName = "variables"
    }
    stages
    {
        stage("Paso 1")
        {
            step
            {
                script { sh "echo 'Hello Word'"}
            }
        }
        stage("Paso 2")
        {
            step
            {
                script { sh "echo 'Hello Live'"}
            }
        }
    }
    post
    {
        always { deleteDir() sh "echo 'Fase Always'"}
        success { sh "echo 'Fase Success'"}
        failure { sh "echo 'Fase Failure'"}
    }
}