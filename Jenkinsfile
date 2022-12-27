node {
    stage('Cont.Downloads') {
    git 'https://github.com/venkat9822891/new-proj.git'
                           }
    stage('Cont.Builds') {
    sh 'mvn package'
                        }
    stage('Cont.Deployments') {
    deploy adapters: [tomcat8(credentialsId: '9f73153b-925c-462c-9a0e-75f094b1ca02', path: '', url: 'http://13.233.91.173:8080/')], contextPath: '/dev-icici', war: '**/*.war'
                          }
}
