pipeline {
  agent any

  environment {
    DEV_NAME = "Rhisland"
  }

  stages {
    stage('Cloner le dépôt') {
      steps {
        git 'https://github.com/wiirhis/jenkins-hello-pipeline'
      }
    }

    stage('Afficher un message') {
      steps {
        echo "Bienvenue ${env.DEV_NAME} dans ton pipeline CI 🎯"
      }
    }

    stage('Lister les fichiers') {
      steps {
        sh 'ls -l'
      }
    }
  }

  post {
    always {
      echo "Fin du pipeline (succès ou échec)"
    }
    success {
      echo "Le pipeline a réussi ✅"
    }
    failure {
      echo "Le pipeline a échoué ❌"
    }
  }
}
