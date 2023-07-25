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
* javax 패키지 이름을 jakarta로 변경해야 합니다.
오라클과 자바 라이센스 문제로 모든 javax 패키지를 jakarta로 변경하기로 했습니다. 3. H2 데이터베이스를 2.1.214 버전 이상 사용해주세요.
패키지 이름 변경 예) JPA 애노테이션
javax.persistence.Entity jakarta.persistence.Entity 스프링에서 자주 사용하는 @PostConstruct 애노테이션
javax.annotation.PostConstruct jakarta.annotation.PostConstruct
스프링에서 자주 사용하는 검증 애노테이션
javax.validation jakarta.validation
