node {   
    stage('Clone repository') {
        git credentialsId: 'git', url: 'https://github.com/phucgo240699/cicd.git'
    }
    
    stage('Build image') {
       dockerImage = docker.build("jaywalker99/cicd:latest")
    }
    
 stage('Push image') {
        withDockerRegistry([ credentialsId: "jaywalker99", url: "" ]) {
        dockerImage.push()
        }
    }    
}
