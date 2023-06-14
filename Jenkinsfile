pipeline {
    agent {
  label 'ansible'
    }
    stages {
        stage('First') {
            steps { 
                sh '/bin/bash'
            }
        }
        stage ('Second') {
            steps {
                sh 'sudo sed -i \'s/vector-role/multibranch pipeline/\' molecule/centos_7/converge.yml'
            }
        }
        stage ('Third') {
            steps { 
                sh 'molecule test -s centos_7'
            }
        }
    }
}
