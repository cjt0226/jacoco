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
    stage('compile spring'){
        dir('spring-boot-test/springboot'){
            sh "mvn compile"
        }
    }
    stage('fecth codecoverage'){
        sh "ant dump"
    }
    stage('generate report'){
        jacoco()
    }
    stage('sonarqube'){
        def scannerHome = tool 'SonarQube Scanner';
        withSonarQubeEnv() {
            sh "${scannerHome}/bin/sonar-scanner"
        }
    }
}