pipeline {
    agent any

    stages {
         stage('Security Scan') {
            steps {
                script {
                    synopsys_scan product: "polaris", polaris_server_url: "https://poc.polaris.synopsys.com", polaris_access_token: "s4jpgckfat47f3dcaebrc486li9tn9a59onks8d0f0t2p1rioudln27nsbemmun4ltpgv0d50iqak", 
                    polaris_application_name: "guava", 
                    polaris_project_name: "1.0", polaris_branch_name: "master", polaris_assessment_types: "SCA, SAST"
                }
            }
        }
    }
}
