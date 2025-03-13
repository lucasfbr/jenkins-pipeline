pipeline {
    agent any
    stages {
        stage('step1') {
            steps {
               script {
                    withCredentials(string(credentialsId: 'NEXT_PUBLIC_API_URL', variable: 'NEXT_PUBLIC_API_URL')) {
                        echo 'step 1'
                        echo "API URL BASE: ${NEXT_PUBLIC_API_URL}"
                    }
                }
            }
            
        }
        stage('step2') {
            steps {
               script {
                    withCredentials(string(credentialsId: 'NEXT_PUBLIC_API_URL', variable: 'NEW_URL')) {
                        echo 'step 2'
                        echo "API URL BASE COM VARIAVEL: ${NEW_URL}"
                    }
                }
            }
        }
        stage('step3') {
            steps {
                echo 'step 3'
            }
        }
    }
}
