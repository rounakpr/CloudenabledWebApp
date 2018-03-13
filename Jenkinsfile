node('mySlave1') {

stage('Clone the repo')
git 'https://github.com/rounakpr/CloudenabledWebApp.git'

stage('Install Maven Tomcat Groovy')
sh 'sudo apt-get install maven tomcat8 groovy -y' 

stage('Maven Package')
sh 'mvn package'

stage('Archive  the Artifact')
archiveArtifacts 'target/*.war'

stage('Deploy the Artifact')
sh 'sudo cp target/CloudenabledWebApp.war /var/lib/tomcat8/webapps'

}
