pipeline
{
    agent any
    stages
    {
        stage('FetchStage')
        {
            steps
            {
                git 'https://github.com/Fhall92/JenkinsAssignment'
            }
        }
        stage('BuildStage') { 
            steps {
                bat 'javac -cp junit-4.13.jar; Student.java studentTest.java'
            }
        } 
        stage('TestStage') { 
            steps {
                bat 'java -cp junit-4.13.jar; org.junit.runner.JUnitCore studentTest'
            }
        }   
    }
}