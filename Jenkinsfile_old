pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                echo 'Cloning repository...'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building...'
                // Add build commands here
            }
        }

        stage('Test') {
            steps {
                echo 'Testing...'
                // Add test commands here
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // Add deployment commands here
            }
        }


        stage('Security Scan') {
            steps {
                script {
                    synopsys_scan product: "polaris", polaris_server_url: "https://polaris.synopsys.com", polaris_access_token: "b67ens83eh4ot0osev3src0qg696afh3vbm4dgcber9sg36p8gen3e9g00g0eedvc18oo5pi5g3g0", 
                    polaris_application_name: "KyleH", 
                    polaris_project_name: "Guava", polaris_branch_name: "master", polaris_assessment_types: "SCA, SAST"
            }
        }
    }
}
    }
