## SpringBoot

비교적 복잡한 Spring Framework의 환경설정을 자동화로 쉽게 할 수 있고 사용법도 간단하다.<br/>
스프링부트 starter dependency만 추가해 주면 API정의 및 내장서버 실행 등 대부분의 설정이 자동화 되기 때문이다.<br/>
뿐만아니라, 의존성 관리도 별도의 작업없이 바로 코딩을 시작할 수 있다는 장점이 있음.

- Spring Boot 내부에 내장서버(tomcat)를 가지고 있음
- starter를 통한 dependency 자동화
- xml 설정하지 않아도 됨
- jar 파일의 자바 옵션만으로 배포가 가능함
- spring actuator를 통해 어플리케이션의 모니터링과 관리 제공

### SpringBoot Starter
의존성 그룹의 개념.간편하게 dependency를 제공해 준다.<br/>
가장 많이 사용하는 JPA의 경우, pom.xml이나 build.gradle에 코드 한 줄만 추가 해 줘도 필요한 라이브러리를 알아서 import해 온다.

```xml
spring-boot-starter-*
```
* 부분에 원하는 starter 명을 명시해 주면 된다.
