pipeline {
    agent any

    stages{
        stage('checkout') {
            steps {
                script{
                    dir("terraform")
                    {
                        git "https://github.com/deepakkumar1983/devops-automation.git"
                    }
                }
            }
        }
        // stage('Build Maven'){
        //     steps{
        //         checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Java-Techie-jt/devops-automation']]])
        //         sh 'mvn clean install'
        //     }
        // }
//         stage('Build docker image'){
//             steps{
//                 script{
//                     sh 'docker build -t javatechie/devops-integration .'
//                 }
//             }
//         }
//         stage('Push image to Hub'){
//             steps{
//                 script{
//                    withCredentials([string(credentialsId: 'dockerhub-pwd', variable: 'dockerhubpwd')]) {
//                    sh 'docker login -u javatechie -p ${dockerhubpwd}'

// }
//                    sh 'docker push javatechie/devops-integration'
//                 }
//             }
//         }
//         stage('Deploy to k8s'){
//             steps{
//                 script{
//                     kubernetesDeploy (configs: 'deploymentservice.yaml',kubeconfigId: 'k8sconfigpwd')
//                 }
//             }
//         }
    }
}
