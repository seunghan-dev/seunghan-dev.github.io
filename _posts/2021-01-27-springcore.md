---
layout: post
title: Spring의 핵심 기술
category: spring
---

### 기술의 핵심
좋은 객체 지향 애플리케이션 개발을 도와준다.

<br>
### 핵심 기술 (Spring Triangle)
- IoC(Inversion of Control) ~ DI(Dependency Injection)
- AOP(Aspect Oriented Programming)
- PSA(Portable Service Abstraction)

<br>
### IoC
인스턴스의 생성부터 소멸까지의 제어권을 Spring이 관리한다.<br>
어떤 객체가 사용할 객체(의존 관계인 객체)를 직접 만드는 것이 아닌, (생성자, 필드에 직접, Setter)를 통해 주입 받아 사용하는 것(DI)

<br>
**Spring IoC 컨테이너**

e.g. ApplicationContext (BeanFactory)

- IoC 기능 제공, Bean을 담고 있음
- Bean을 만들고, 엮고, 제공
- 기본적으로 싱글톤으로 등록

<br>
### AOP
관점 지향 프로그래밍 - Aspect(여러 군데서 사용되는 코드)를 분리하여 관리

<br>
**프록시 패턴**

e.g. @Transaction

- 어떤 기능을 추가할 때, 기존 코드를 변경하지 않고 기능 추가 가능
- 어떤 클래스가 Spring AOP 대상이면, 빈 등록 시 Spring AOP가 프록시를 만들어 기존 클래스 대신 빈으로 등록

<br>
### PSA
추상화 계층을 사용해서 어떤 기술을 내부에 숨기고 개발자에게 편의성 제공 (Service Abstraction) <br>
다른 기술 스택으로 간편하게 바꿀 수 있는 확장성 (Portable)

e.g. @Transaction, Spring web MVC