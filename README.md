# jacoco

### add below info to catalina.sh <br>
JAVA_OPTS="$JAVA_OPTS -javaagent:/Users/frank.chen/Library/jacoco/lib/jacocoagent.jar=includes=*,output=tcpserver,address=*,port=8082 -Xverify:none"
