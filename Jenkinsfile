pipeline {
  agent {
    kubernetes {
      label 'mypodtemplate-v1'
      defaultContainer 'jnlp'
      yamlFile 'mvnAgent.yaml'
    }
  }
  stages {
    stage('Run maven') {
      steps {
        container('maven') {
          sh 'mvn -version'
        }
      }
    }
  }
}
