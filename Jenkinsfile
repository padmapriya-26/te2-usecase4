pipeline {
  agent any

  stages {

    stage('Checkout Code') {
      steps {
        git 'https://github.com/padmapriya-26/te2-usecase4.git'
      }
    }

    stage('Create GCP VM') {
      steps {
        sh 'ansible-playbook ansible/create-vm.yaml'
      }
    }

    stage('Install DevOps Tools') {
      steps {
        sh 'ansible-playbook -i ansible/inv ansible/install tools.yaml'
      }
    }
  }
}
