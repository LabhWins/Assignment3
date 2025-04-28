pipeline {
  agent any

  stages {
    stage('Git Clone Repository') {
        steps {
           git branch: 'main', url: 'https://github.com/LabhWins/Assignment3/Jenkinsfile.git'
        }
    }
    stage('Publish HTML') {
        steps {
            publicHTML(target: [
                reportName            : 'HTML Page',
                reportDir             :  '.',
                reportFiles           : 'index.html',
                keepAll               : true,
                alwaysLinkToLastBuild : true,
                allowMissing          : false,
          ])
        }
    }
  }
}
