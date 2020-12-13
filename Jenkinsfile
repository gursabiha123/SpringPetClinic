pipeline{
    agent{label 'master'}
    tools{maven 'M1'}
    stages{
        stage('first'){
            steps{
                git branch:'main',url:'https://github.com/gursabiha123/SpringPetClinic.git'
                
            }
        }
        stage('second')
        {
            steps{
                sh 'mvn compile'
            }
        }
        stage('tests')
        {
            steps{
                sh 'mvn test'
            }
        }
        stage('Package'){
            steps{
                sh 'mvn package'
            }
        }
        stage('Deploys'){
            steps{
                sh 'java -jar /var/lib/jenkins/workspace/declerativePipeline/target/*.jar'
            }
        }
    }
    
}
