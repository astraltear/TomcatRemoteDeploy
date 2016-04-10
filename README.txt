http://maven.apache.org/plugins/maven-war-plugin/usage.html
Run As>Maven build
	Goals:package
	
http://tomcat.apache.org/maven-plugin-2.2/

TOMCAT_HOME/conf/tomcat-users.xml
<role rolename="manager"/>
<role rolename="manager-gui"/>
<role rolename="manager-script"/>
<role rolename="admin"/>
<user username="tomcat" password="admin" roles="admin,manager,manager-gui,manager-script"/>
 
pom.xml
<plugin>
	<groupId>org.apache.tomcat.maven</groupId>
	<artifactId>tomcat7-maven-plugin</artifactId>
	<version>2.2</version>
	<configuration>
		<url>http://192.168.0.21:8080/manager/text</url>
		<path>/autoDeploy</path>
		<username>tomcat</username>
		<password>admin</password>
	</configuration>
</plugin>

Goal: tomcat7:redeploy
	tomcat7:undeploy tomcat7:deploy
	
http://tomcat.apache.org/maven-plugin-2.2/container-goals.html
