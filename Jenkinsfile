node('wallmart-node1'){
def mavenHome = tool name: "3.8.2"    
stage('checkout code')
{
git branch: 'development', credentialsId: '9e634e68-a74d-4757-8db5-6a635db60e96', url: 'https://github.com/lshanthi/maven-web-application.git'
}
stage('Build')
{
sh "${mavenHome}/bin/mvn clean package"    
} 
/*    
stage('sonarqube report'){
    sh "${mavenHome}/bin/mvn clean sonar:sonar"
}
stage('upload artifact into nexus'){
sh "${mavenHome}/bin/mvn clean deploy"
}
stage('deploy app inti tomcat server'){
sshagent(['415d2971-d0a4-4a5c-844b-d44ae3408a1b']){
sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@34.242.214.18:/opt/apache-tomcat-9.0.59/webapps"
}    
}
stage('send Email notification'){
emailext body: '''Build is over 
Regards,
Prashanthi.
8790575072.''', subject: 'Build over..', to: 'prashanthirajulagidi@gmail.com'    
}
*/
}
