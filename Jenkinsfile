stages {
        stage('deploy k-8') {
            steps {
                withKubeConfig(caCertificate: '', clusterName: 'EKS-1', contextName: '', credentialsId: 'k8-token', namespace: 'webapps', restrictKubeConfigAccess: false, serverUrl: 'https://CD3D86ABAC70D39E865C2563E47E75AF.gr7.us-east-1.eks.amazonaws.com') {
                sh "kubectl -f apply deployment-service.yml"
                sh "sleep 30"                                             }
            }
        }
        
        
        
stage('ckeck k-8') {
            steps {
                withKubeConfig(caCertificate: '', clusterName: 'EKS-1', contextName: '', credentialsId: 'k8-token', namespace: 'webapps', restrictKubeConfigAccess: false, serverUrl: 'https://CD3D86ABAC70D39E865C2563E47E75AF.gr7.us-east-1.eks.amazonaws.com') {
                sh "kubectl get all -n webapps"
                                                        }
            }
        }
    }

