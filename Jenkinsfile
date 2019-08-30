node('docker') {
 
    stage 'Checkout'
        checkout scm
    stage 'Build & UnitTest'
        sh "docker pull jenkins"
        sh "docker pull ubuntu "
  
    stage 'Integration Test'
        sh "docker build -t jenkins"
        sh "docker run -it -d jenkins -p 8080:8080 -p 500000:500000"
}
