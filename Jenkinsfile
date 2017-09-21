pipeline {
  agent {
    node {
      label 'master'
    }
    
  }
  stages {
    stage('CriarProjeto') {
      steps {
        springBoot(selectedIDs: 'web,data-jpa', artifactId: 'demospring', bootVersion: '1.5.7.RELEASE', description: 'Teste de projeto Novo', groupId: 'br.com.basis', packaging: 'jar', projectName: 'demospring', type: 'maven-project')
      }
    }
    stage('Compilar') {
      steps {
        sh '''chown +x mvwn
./mvnw clean package'''
      }
    }
  }
}