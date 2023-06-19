node {   
    stage('Clone repository') {
        git credentialsId: 'github', url: 'https://github.com/deepakbhatt0809/jenkinsdemo'
    }
    
    stage('Build image') {
       dockerImage = docker.build("deepakbhatt07/jenkinsdemo:latest")
    }
    
 stage('Push image') {
        withDockerRegistry([ credentialsId: "dockerhub", url: "" ]) {
        dockerImage.push()
        }
    }    
}
