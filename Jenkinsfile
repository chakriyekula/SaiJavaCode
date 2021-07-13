pipeline{
    agent any
    stages{
        stage('git clone')
        {
            steps
            {
                git credentialsId: 'github', url: 'https://github.com/chakriyekula/SaiJavaCode.git'
            }
        }
        stage('build')
        {
            steps
            {
                bat "mvn clean install package" 
            }
        }
        stage('copy war')
        {
            steps
            {
                bat "copy C:\\Windows\\System32\\config\\systemprofile\\AppData\\Local\\Jenkins\\.jenkins\\workspace\\pipeline_job\\webapp\\target\\*war C:\\Users\\SONY\\Downloads\\apache-tomcat-9.0.48\\webapps" 
            }
        }
    }
}
