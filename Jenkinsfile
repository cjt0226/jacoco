node('codecoverage'){
    stage ('checkcout SCM'){
        cleanWs()
        checkout scm
    }
    stage('fetch'){
        dir('jacoco'){
            git url:'https://github.com/cjt0226/jacoco.git'
        }
        dir('spring-boot-test'){
            git url:'https://github.com/cjt0226/spring-boot-test.git'
        }
    }
}