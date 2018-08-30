
## HealerJean的梦想博客


## 规范

#### 1、groupId `com.hlj.repo`
#### 2、artifactId 工具类名字
#### 3、版本 0.0.1（初始）


```
	<repositories>
		<repository>
			<!--id任意-->
			<id>hlj-repo</id>
			<url>https://raw.github.com/HealerJean123/maven_github/master/hlj-test-github-maven</url>
		</repository>
	</repositories>
```

举例

```
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
	<modelVersion>4.0.0</modelVersion>

	<groupId>com.hlj.repo</groupId>
	<artifactId>test-github-maven</artifactId>
	<version>0.0.1</version>
	<packaging>jar</packaging>

	<name>com-hlj-github-maven-repo</name>
	<description>Demo project for Spring Boot</description>

	<parent>
		<groupId>org.springframework.boot</groupId>
		<artifactId>spring-boot-starter-parent</artifactId>
		<version>2.0.4.RELEASE</version>
		<relativePath/> <!-- lookup parent from repository -->
	</parent>

	<properties>
		<project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
		<project.reporting.outputEncoding>UTF-8</project.reporting.outputEncoding>
		<java.version>1.8</java.version>
		<distributionManagement.directory.name>hlj-test-github-maven</distributionManagement.directory.name>

	</properties>

	<distributionManagement>
		<repository>
			<id>hlj-managemaent-Id</id>
			<name>hlj managemaent name</name>
			<url>file://${project.build.directory}/${distributionManagement.directory.name}</url>
		</repository>
	</distributionManagement>

	<repositories>
		<repository>
			<!--id任意-->
			<id>hlj-repo</id>
			<url>https://raw.github.com/HealerJean123/maven_github/master/hlj-test-github-maven</url>
		</repository>
	</repositories>

	<dependencies>


		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter</artifactId>
		</dependency>

		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-test</artifactId>
			<scope>test</scope>
		</dependency>

		<!--github仓库导入的-->
		<dependency>
			<groupId>com.hlj.repo</groupId>
			<artifactId>test-github-maven</artifactId>
			<version>0.0.1</version>
		</dependency>
	</dependencies>

	<build>
		<plugins>
			<plugin>
				<groupId>org.springframework.boot</groupId>
				<artifactId>spring-boot-maven-plugin</artifactId>
			</plugin>

			<!--maven发布插件-->
			<plugin>
				<artifactId>maven-deploy-plugin</artifactId>
				<version>2.8.1</version>
				<configuration>
					<altDeploymentRepository>internal.repo::default::file://${project.build.directory}/${distributionManagement.directory.name}</altDeploymentRepository>
				</configuration>
			</plugin>
		</plugins>
	</build>


</project>

```

<br/><br/><br/>
如果满意，请打赏博主任意金额，感兴趣的在微信转账的时候，添加博主微信哦， 请下方留言吧。可与博主自由讨论哦

|支付包 | 微信|微信公众号|
|:-------:|:-------:|:------:|
|![支付宝](https://raw.githubusercontent.com/HealerJean123/HealerJean123.github.io/master/assets/img/tctip/alpay.jpg) | ![微信](https://raw.githubusercontent.com/HealerJean123/HealerJean123.github.io/master/assets/img/tctip/weixin.jpg)|![微信公众号](https://raw.githubusercontent.com/HealerJean123/HealerJean123.github.io/master/assets/img/my/qrcode_for_gh_a23c07a2da9e_258.jpg)|


