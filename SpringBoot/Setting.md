# 스프링 환경설정

## 사전 준비물
- Java 11 설치
- IDE: IntelliJ 또는 Eclipse 설치
> 주의! 가급적 JDK 11 버전을 설치해주세요. 다른 버전을 설치하면 정상 동작하지 않을 가능성이 높습니다.

* [스프링 부트 스타터 사이트](https://start.spring.io)로 이동해서 스프링 프로젝트 생성

* **프로젝트 선택**
   * Project: Gradle - Groovy Project Spring Boot: 2.3.x
   * Language: Java
   * Packaging: Jar
   * Java: 11 Project Metadata
   * groupId: hello
   * artifactId: hello-spring Dependencies: Spring Web, Thymeleaf
   * 주의! - 스프링 부트 3.0
   * 스프링 부트 3.0을 선택하게 되면 다음 부분을 꼭 확인해주세요. 1. Java 17 이상을 사용해야 합니다.

* **build.gradle** 기본설정
```java
plugins {
id 'java'
id 'org.springframework.boot' version '2.7.11'
id 'io.spring.dependency-management' version '1.0.15.RELEASE'
}

group = 'hello'
version = '0.0.1-SNAPSHOT'
sourceCompatibility = '11'

repositories {
	mavenCentral()
}

dependencies {
	implementation 'org.springframework.boot:spring-boot-starter-thymeleaf'
	implementation 'org.springframework.boot:spring-boot-starter-web'
	testImplementation 'org.springframework.boot:spring-boot-starter-test'
}

tasks.named('test') {
	useJUnitPlatform()
}
```

J
