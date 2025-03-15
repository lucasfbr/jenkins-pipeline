pipeline {
    agent any
    stages {
         stage('step1') {
            steps {
                echo 'step 1'
                echo "Iniciando verificação de variaveis de ambiente"
                echo "variaveis do sistema e não do jenkins:"
                echo "Host do projeto: ${env.SPRING_DATASOURCE_URL}"
                echo "User: ${env.SPRING_DATASOURCE_USERNAME}"
                echo "Password: ${env.SPRING_DATASOURCE_PASSWORD}"
            }
        }
        stage('step2') {
            steps {
               script {
                    withCredentials([string(credentialsId: 'NEXT_PUBLIC_API_URL', variable: 'NEXT_PUBLIC_API_URL')]) {
                        echo 'step 2'
                        echo "API URL BASE: ${NEXT_PUBLIC_API_URL}"
                    }
                }
            }
        }
        stage('step3') {
            steps {
               script {
                    withCredentials([string(credentialsId: 'NEXT_PUBLIC_API_URL', variable: 'NEW_URL')]) {
                        echo 'step 3'
                        echo "API URL BASE COM VARIAVEL: ${NEW_URL}"
                    }
                }
            }
        }
    }
}
