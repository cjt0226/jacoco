node('codecoverage'){
    stage ('checkcout SCM'){
        cleanWs()
        checkout scm
    }
    stage('fetch'){
        dir('spring-boot-test'){
            git url:'https://github.com/cjt0226/spring-boot-test.git'
        }
    }
}