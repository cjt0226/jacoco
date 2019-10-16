# jacoco



### 1.pre-condition:
1.tomcat 在/Users/{username}/Library/tomcat<br>
2.add below info to catalina.sh<br>
JAVA_OPTS="$JAVA_OPTS -javaagent:/Users/frank.chen/Library/jacoco/lib/jacocoagent.jar=includes=\*,output=tcpserver,address=\*,port=8082 -Xverify:none"<br>
3.jenkins node 需要安装java，maven,jacoco(/opt/jacoco)。且节点指定JAVA_HOME<br>
<br>
### 2.Change:
1.端口变动需要修改catalina.sh中agent的端口和build.xml中的端口<br>
2.tomcat server变动需要更改build.xml的server_ip<br>
