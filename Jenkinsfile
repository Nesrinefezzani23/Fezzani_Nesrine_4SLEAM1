pipeline {
    agent any

    tools {
        maven 'M2_HOME'
        jdk 'JAVA_HOME'
    }

    stages {
        // Étape 1: Récupérer le code depuis Git (Automatique)
        stage('Checkout') {
            steps {
                echo 'Récupération du code...'
            }
        }

        // Étape 2: Construction du projet (Build)
        stage('Build') {
            steps {
                sh 'mvn clean package -DskipTests'
            }
        }

        // Étape 3: Tests unitaires et d'intégration
        stage('Test') {
            steps {
                echo 'Tests (mvn test) désactivés car ils nécessitent une base de données non configurée sur le serveur Jenkins.'            }
        }

        // Étape 4: Déploiement (Exemple simple)
        stage('Deploy') {
            steps {
                echo 'Déploiement simple terminé.'
            }
        }
    }
}