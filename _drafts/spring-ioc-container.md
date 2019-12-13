---
layout: post
title: "[Spring] IoC 컨테이너"
description: "스프링 프레임워크 핵심 기술(백기선) 공부한 내용 정리"
category: articles
tags: [java, spring]
comments: true
---

# IoC 컨테이너

## IoC 란?

- Inversion of Control : 어떤 객체가 사용하는 의존 객체를 직접 만들어서 사용하는게 아니라 주입 받아 사용하는 방법, DI(Dependency Injection) 이라고도 함

## 스프링 IoC 컨테이너

- [BeanFactory](https://docs.spring.io/spring-framework/docs/5.0.8.RELEASE/javadoc-api/org/springframework/beans/factory/BeanFactory.html) : 스프링 IoC 컨테이너 최상위 인터페이스
- 어플리케이션 컴포넌트의 중앙 저장소
- [Bean](#Bean) 설정 소스(혹은 xml)으로부터 빈 정의를 읽어, 빈을 구성하고 제공함)

## Bean

- Bean<sup id="bean">[\[1\]](#footnote1)</sup> 이란? : **스프링 Ioc 컨테이너가 관리** 하는 객체
- 의존성 주입을 위해 관리되는 대상
- Bean은 기본적으로 싱글톤 스코프로 객체를 만들어 사용 <-> 프로토타입, 매번 다른 객체 생성
- 라이프사이클 인터페이스 지원 - **_추가 공부 필요_**

## [ApplicationContext](https://docs.spring.io/spring-framework/docs/5.0.8.RELEASE/javadoc-api/org/springframework/context/ApplicationContext.html)

- BeanFactory 상속받은 구현체
- 추가적으로 ApplicationEventPublisher, BeanFactory, EnvironmentCapable, HierarchicalBeanFactory, ListableBeanFactory, MessageSource, ResourceLoader, ResourcePatternResolver을 상속 받음

---

[\[<b id="footnote1">1</b>\]](#bean) 내용
