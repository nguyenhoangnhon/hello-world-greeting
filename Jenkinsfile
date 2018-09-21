node {
  stage('Poll') {
    checkout scm
  }
 stage('SonarQube analysis') {
    // requires SonarQube Scanner 2.8+
    def scannerHome = tool 'Default SonarQube Server';
    withSonarQubeEnv('Default SonarQube Server') {
       sh 'mvn org.sonarsource.scanner.maven:sonar-maven-plugin:3.2:sonar'
    }
  }
}
