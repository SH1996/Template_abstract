开发环境mac OS：
=============
	1).下载eclipse，JDK，maven，tomcat（建议Eclipse最新，JDK1.8，maven3.5，tomcat8）
  
	2).配置环境变量（JDK，maven）在用户文件夹之下shift+command+.打开.bash_profile：
  
		#maven安装目录
		MAVEN_HOME=/Users/a1/Downloads/apache-maven-3.5.3
		#将maven安装目录的bin目录添加到path路径变量
		PATH=$PATH:$MAVEN_HOME/bin
		export PATH=${PATH}:/usr/local/mysql/bin
		export PATH=$PATH:/Users/a1/Downloads/apache-tomcat-7.0.85/bin
		#配置JDK环境变量
		JAVA_HOME=/Library/Java/JavaVirtualMachines/jdk1.8.0_131.jdk/Contents/Home
		PATH=$JAVA_HOME/bin:$PATH
		CLASSPATH=.:%JAVA_HOME/bin/dt.jar:$JAVA_HOME/lib/tools.jar
		export JAVA_HOME PATH CLASSPATH

	3).terminal.app测试java -version和mvn -version，是否配置成功
	4).设置：https://blog.csdn.net/bluewindtalker/article/details/54562255
	5).安装maven：网上教程，重点解决maven报：
		（- Plugin execution not covered by lifecycle configuration: 				org.apache.maven.plugins:maven-resources-plugin:2.6:testResources 			(execution: default- 	 testResources, phase: process-test-resources) 	- 		Plugin execution not covered by lifecycle configuration）: 错问题；
			1.删除m2e插件，重新安装，建议在marksplace中安装，原因版本不一
			2.add pluging(添加所有maven需要的插件包)，因为maven是有很多插件构成				3.update project；
(第二步导入pom.xml的内容剪切)
```
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
  <modelVersion>4.0.0</modelVersion>
  <groupId>itcast0907crmCache</groupId>
  <artifactId>itcast0907crmCache</artifactId>
  <version>0.0.1-SNAPSHOT</version>
  <packaging>war</packaging>
  <build>
  <pluginManagement>
  	<plugins>
  		<plugin>
  			<groupId>org.apache.maven.plugins</groupId>
  			<artifactId>maven-resources-plugin</artifactId>
  			<version>2.6</version>
  		</plugin>
  		<plugin>
  			<groupId>org.apache.maven.plugins</groupId>
  			<artifactId>maven-surefire-plugin</artifactId>
  			<version>2.12.4</version>
  		</plugin>
  		<plugin>
  			<groupId>org.apache.maven.plugins</groupId>
  			<artifactId>maven-war-plugin</artifactId>
  			<version>3.0.0</version>
  		</plugin>
  		<plugin>
  			<groupId>org.apache.maven.plugins</groupId>
  			<artifactId>maven-compiler-plugin</artifactId>
  			<version>3.5.1</version>
  		</plugin>
  		<plugin>
  			<groupId>org.apache.maven.plugins</groupId>
  			<artifactId>maven-install-plugin</artifactId>
  			<version>2.4</version>
  		</plugin>
  		<plugin>
  			<groupId>org.apache.maven.plugins</groupId>
  			<artifactId>maven-jar-plugin</artifactId>
  			<version>2.4</version>
  		</plugin>
  	<plugin>
  		<groupId>org.apache.maven.plugins</groupId>
  		<artifactId>maven-clean-plugin</artifactId>
  		<version>2.5</version>
  	</plugin>
  	<plugin>
  		<groupId>org.apache.maven.plugins</groupId>
  		<artifactId>maven-deploy-plugin</artifactId>
  		<version>2.7</version>
  	</plugin>
  	<plugin>
  		<groupId>org.apache.maven.plugins</groupId>
  		<artifactId>maven-site-plugin</artifactId>
  		<version>3.3</version>
  	</plugin>
  	<plugin>
  		<groupId>org.apache.maven.plugins</groupId>
  		<artifactId>maven-clean-plugin</artifactId>
  		<version>2.5</version>
  	</plugin>
  	</plugins>
  </pluginManagement>	
  <plugins>
  	<plugin>
  		<groupId>org.apache.maven.plugins</groupId>
  		<artifactId>maven-resources-plugin</artifactId>
  	</plugin>
  	<plugin>
  		<groupId>org.apache.maven.plugins</groupId>
  		<artifactId>maven-compiler-plugin</artifactId>
  	</plugin>
  	<plugin>
  		<groupId>org.apache.maven.plugins</groupId>
  		<artifactId>maven-clean-plugin</artifactId>
  	</plugin>
  	<plugin>
  		<groupId>org.apache.maven.plugins</groupId>
  		<artifactId>maven-deploy-plugin</artifactId>
  	</plugin>
  	<plugin>
  		<groupId>org.apache.maven.plugins</groupId>
  		<artifactId>maven-install-plugin</artifactId>
  	</plugin>
  	<plugin>
  		<groupId>org.apache.maven.plugins</groupId>
  		<artifactId>maven-jar-plugin</artifactId>
  	</plugin>
  	<plugin>
  		<groupId>org.apache.maven.plugins</groupId>
  		<artifactId>maven-site-plugin</artifactId>
  	</plugin>
  	<plugin>
  		<groupId>org.apache.maven.plugins</groupId>
  		<artifactId>maven-surefire-plugin</artifactId>
  	</plugin>
  	<plugin>
  		<groupId>org.apache.maven.plugins</groupId>
  		<artifactId>maven-war-plugin</artifactId>
  	</plugin>
  </plugins>
  </build>
</project>
```
6).安装其它插件：STS，Angular JS，等

7).myeclipse的安装破解说明：访问（链接:https://pan.baidu.com/s/1QW2zY-vhWsG91uGPSzg9iA  密码:ydoh）.
