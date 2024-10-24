node() {
   stage('Download the code from Git') 
               {
    git branch: 'dev', url: 'https://github.com/ash09-SaaS/oct24-code.git'
                }
    stage('Convert into artifacts') {
   sh 'mvn package'
                }
    stage('deploy into container') {
   deploy adapters: [tomcat9(credentialsId: 'f7b57967-66b3-4419-b513-0760c8419a67', path: '', url: 'http://13.201.225.102:8080/')], contextPath: '/jenkins-dev-aap', war: '**/*.war'
}

}
