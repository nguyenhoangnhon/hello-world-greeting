node {
  stage('Poll') {
    checkout scm
  }
 stage('SonarQube analysis') {
    // requires SonarQube Scanner 2.8+
    def scannerHome = tool 'Default SonarQube Server';
    withSonarQubeEnv('Default SonarQube Server') {
      sh "${scannerHome}/bin/sonar-scanner"
    }
  }
}
