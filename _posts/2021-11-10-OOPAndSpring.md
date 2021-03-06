---
title: "객체 지향 프로그래밍과 스프링"
categories: ['Java']
---

# 객체 지향 프로그래밍(OOP, Object-Oriented Programming)

- 컴퓨터 프로그램을 명령어의 목록으로 보는 시각에서 벗어나 여러 개의 독립된 단위, 즉  "객체"들의 모임으로 파악하고자 하는 것
- 각각의 객체는 메시지를 주고받고, 데이터를 처리할 수 있음(협력)
- 객체 지향 프로그래밍은 프로그램을 유연하고 변경이 용이하게 만들기 때문에 대규모 소프트웨어 개발에 많이 사용됨
- 레고 블록 조립하듯이, 컴퓨터 부품을 갈아 끼우듯이, 컴포넌트를 쉽고 유연하게 변경하면서 개발할 수 있는 방법(다형성)
- 역할과 구현을 분리
  - 역할과 구현으로 구분하면 세상이 단순해지고, 유연해지면서 변경도 편리해짐
  - 장점
    - 클라이언트는 대상의 역할(인터페이스)만 알면 됨
    - 클라이언트는 구현 대상의 내부 구조를 몰라도 됨
    - 클라이언트는 구현 대상의 내부 구조가 변경되어도 영향을 받지 않음
    - 클라이언트는 구현 대상 자체를 변경해도 영향을 받지 않음
  - 자바 언어의 다형성을 활용
    - 역할 = 인터페이스
    - 구현 = 인터페이스를 구현할 클래스, 구현 객체
  - 객체를 설계할 때 역할과 구현을 명확히 분리
  - 객체 설계 시 역할(인터페이스)을 먼저 부여하고, 그 역할을 수행하는 구현 객체 만들기
  - 정리
    - 실세계의 역할과 구현이라는 편리한 컨셉을 다형성을 통해 객체 세상으로 가져올 수 있음
    - 유연하고 변경이 용이
    - 확장 가능한 설계
    -  클라이언트에 영향을 주지 않는 변경 가능
    - 인터페이스를 안정적으로 잘 설계하는 것이 중요
- 객체의 협력
  - 혼자 있는 객체는 없음
  - 클라이언트 : 요청
  - 서버 : 응답
  - 수많은 객체 클라이언트와 객체 서버는 서로 협력 관계를 가짐
- 스프링과 객체 지향
  - 다형성이 가장 중요
  - 스프링은 다형성을 극대화해서 이용할 수 있게 도와줌
  - 스프링에서 이야기하는 제어의 역전(IoC), 의존관계 주입(DI)은 다형성을 활용해서 역할과 구현을 편리하게 다룰 수 있도록 지원함
  - 스프링을 사용하면 마치 레고 블록 조립하듯이, 공연 무대의 배우를 선택하듯이 구현을 편리하게 변경할 수 있음
- 좋은 객체 지향 설계의 5가지 원칙(SOLID)
  - 클린 코드로 유명한 로버트 마틴이 좋은 객체 지향 설계의 5가지 원칙을 정리
  - SRP(단일 책임 원칙, Single Responsibility Principle)
    - 한 클래스는 하나의 책임만 가져야 함
    - 변경이 있을 때 파급 효과가 적으면 단일 책임 원칙을 잘 따른 것
  - OCP(개방-폐쇄 원칙, Open/closed Principle)
    - 소프트웨어 요소는 확장에는 열려 있으나 변경에는 닫혀 있어야 함
    - 다형성 활용 -> 인터페이스를 구현한 새로운 클래스를 만들어서 새로운 기능을 구현
    - 문제점 
      - 구현 객체를 변경하려면 클라이언트 코드를 변경해야 함
      - 다형성을 사용했지만 OCP 원칙을 지킬 수 없음
        ​	-> 객체를 생성하고 연관 관계를 맺어주는 별도의 조립, 설정자 필요 
  - LSP(리스코프 치환 원칙, Liskov Substitution Principle)
    - 프로그램의 객체는 프로그램의 정확성을 깨뜨리지 않으면서 하위 타입의 인스턴스로 바꿀 수 있어야 함
    - 다형성에서 하위 클래스는 인터페이스 규약을 다 지켜야 한다는 것, 다형성을 지원하기 위한 원칙, 인터페이스를 구현한 구현체는 믿고 사용하려면 이 원칙이 필요함
  - ISP(인터페이스 분리 원칙, Interface Segregation Principle)
    - 특정 클라이언트를 위한 인터페이스 여러 개가 범용 인터페이스 하나보다 나음
    - 인터페이스가 명확해지고, 대체 가능성이 높아짐
  - DIP(의존관계 역전 원칙, Dependency Inversion Principle)
    - 프로그래머는 추상화에 의존해야지 구체화에 의존하면 안 된다.
      ​	 -> 구현 클래스에 의존하지 말고 인터페이스에 의존하라는 뜻





# 스프링(Spring)
- 스프링이 다형성과 OCP, DIP를 가능하게 하는 기술
  - DI(Dependency Injection) : 의존관계, 의존성 주입
  - DI 컨테이너 제공
- 클라이언트 코드의 변경 없이 기능 확장
- 쉽게 부품을 교체하듯이 개발 
- 인터페이스를 무분별하게 남발하면 추상화라는 비용이 발생함
- 기능을 확장할 가능성이 없다면 구체 클래스를 직접 사용하고 향후 꼭 필요할 때 리팩터링해서 인터페이스를 도입하는 것도 좋은 방법
