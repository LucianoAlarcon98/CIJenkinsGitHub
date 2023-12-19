pipeline {
    agent any
    
    tools {
        maven "maven-nodo-principal"
    }

    stages {
        stage('Checkout') {
            steps {
                // Puedes añadir aquí cualquier paso necesario para la obtención del código fuente.
                checkout scm
            }
        }
        stage('Build and Test') {
            steps {
                script {
                    // Utiliza el comando Maven para construir y probar el proyecto.
                    // Asegúrate de ajustar los parámetros según tus necesidades.
                    def mavenHome = tool 'maven-nodo-principal'
                    sh "${mavenHome}/bin/mvn clean install"
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                // Agrega los pasos de implementación aquí si es necesario
            }
        }
    }
}
