node('codecoverage'){
    stage ('checkcout SCM'){
        cleanWs()
        checkout scm
    }
    stage('fetch'){
        git url:'https://github.com/cjt0226/spring-boot-test.git'
    }
}