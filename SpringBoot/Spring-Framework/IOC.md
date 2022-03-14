### IOC (Inversion Of Control)
메소드나 객체의 호출을 개발자가 결정하지 않고, 컨테이너가 결정함.<br/>
Spring의 컨테이너는 Spring Bean과 인스턴스들의 생성,관계,생명주기를 관리하며 컨테이너에 등록된 것은 자유롭게 사용가능하다.<br/>
개발자로 부터 처리권한을 위임받았다고 볼수 있다.
<br/>

> java에서의 객체 생성 
```java
 Bookstore bookstore = new Bookstore();
 //new 연산자로 생성
```

> Spring에서의 객체 생성
```java
setter(수정자) 또는 생성자
//외부에 객체를 생성한 뒤 수정자나 생성자로 생성하고자 하는 객체를 주입하는 방식
```
객체를 개발자가 직접 생성하지 않고 컨테이너를 통해 객체를 생성 또는 관리하기 때문에 제어방식이 역전된 것.<br/>
직관적이지 못하기 때문에 의존성 주입(DI)를 통해 구현한다.<br/>

### 컨테이너란?
  - 인스턴스의 생명주기를 관리하고 추가적인 기능을 제공함.
    - 빈팩토리 : DI의 기본사항 제공하는 가장 단순한 컨테이너. Bean을 생성하고 분해하는 책임을 진다.
    - 어플리케이션 컨텍스트 : 빈팩토리와 유사하지만 좀 더 많은기능 제공

### bean
스프링 컨테이너에 의해 생성되고 관계설정, 사용제어를 담당하는 오브젝트

### bean factory 
스프링의 IOC를 담당하는 핵심 컨테이너.

### application context
bean factory에서 확장된 IOC 컨테이너.<br/>
ApplicationContext 는 application context가 구현해야 하는 인터페이스이고 bean factory를 상속함

### configuration metadata
application context 혹은 bean factory가 IOC를 적용하기 위해 사용하는 메타데이터



