node
{
def mavenHOme = tool name: "maven3.8.4"
stage('CheckoutCode')
{
    git branch: 'development', credentialsId: '0ea2bd6e-afd1-4910-bf58-ce166987d485', 
    url: 'https://github.com/novbatch-github-vk/maven-web-application.git'

}
stage('Build'){
sh "${mavenHOme}/bin/mvn clean package"
}
 /*   
stage('ExecuteSQReport'){
sh "${mavenHOme}/bin/mvn clean sonar:sonar"
}
stage('uploadArtifacroryintoNexus'){
sh "${mavenHOme}/bin/mvn clean deploy"
}
stage('DeployAppintoTomcat'){
sshagent(['90e239fc-084d-4ab1-bfbb-907d0a03d4b8']) {
    sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@15.206.157.66:/opt/apache-tomcat-9.0.56/webapps/"
}		
}
stage('SendNotifications'){
emailext body: '''Build over....

Regards,
vijay k''', subject: 'Build over', to: 'vijaykotikal198@gmail.com'
}
*/
}
