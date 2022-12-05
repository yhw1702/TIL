# TIL

>오늘 배운 것을 기록합니다.

<details>
  <summary>2022 10 20( Semaphore와 Mutex )</summary>
<pre>

# 2. Semaphore와 Mutex

동기화 기법의 대표적인 방법 두 가지

## 2-1 세마포어(Semaphore)
특정 변수를 통해서 공유 자원에 접근을 제한하는 방식입니다. 예를들어 세마포어로 사용할 값이 1이상이면 임계구역에 
접근 가능하고 0이면 자원에 더 이상 접근을 할 수 없는 방식입니다.

## 2-2 뮤텍스(Mutex)
Mutual extension의 줄임말로 상호배제라고 합니다. 오직 하나의 프로세스만 임계구역에 대해 접근이 가능하며, 임계구역에 
접근하여 사용중일때는 Lock을 걸어 다른 프로세스가 접근하지 못하도록 하는 것을 의미합니다. 프로세스가 임계구역접근을 
해제해야만 다른 프로세스가 접근을 할 수 있습니다.

## 2-3 차이점
뮤텍스는 단 1개의 프로세스만 접근이 가능한 동기화 방법이며 그에 반해 세마포어의 값은 1보다 큰 값으로 관리할 수 있습니다. 
그리고 세마포어는 임계구역을 사용중인 프로세스 뿐 아니라 다른 프로세스 및 스레드도 세마포어 값을 변경할 수 있는 반면, 
뮤텍스는 Lock한 프로세스 만이 Unlock이 가능합니다.

</pre>
</details>


<details>
  <summary>스프링부트 개념정리(1)</summary>
<pre>

# 스프링은?
1. frame work임
2. 오픈소스 - 소스가 공개되어 있음(뜯어고칠 수 있음)
3. IoC(Inversion of Controll - 제어의 역전) 컨테이너를 가진다.
  * 주도권이 스프링에 있다.
  * 메서드나 객체의 호출 작업을 개발자가 아닌 '외부'에서 결정하는 것
4. DI(Dependency Injection)를 지원한다.
  * 클래스 내에서 사용되는 객체의 생성은 코드로 직접하지 않고 외부로부터 주입받음
5. 많은 필터를 가지고 있다.
6. 많은 어노테이션이 있다. 
7. MessageConverter를 가짐 기본값은 Json 
  * MessageConverter : 중간언어로 변경해주는 스프링 라이브러리
8. BufferedReader와 BufferedWriter를 쉽게 사용가능

# JPA(Java Persistence API)란?
1. 인터페이스이다.( 구현하는 실제 클래스가 필요 ex)Hibernate )
2. ORM(Object Relational Mapping) 기술이다.
  * 객체로 구성한 데이터를 관계형 데이터베이스에 연결(맵핑)하고, 데이터에 대해 쿼리를 보내고 관리를 할 수 있는 도구
3. 반복적인 CRUD 작업을 생략하게 해줌
4. 영속성 컨텍스트를 가지고 있다. (엔티티를 영구 저장하는 환경)
  * 컨텍스트 : 맥락, 대상의 정보
5. DB와 OOP의 불일치성을 해결하기 위한 방법론을 제공한다.(DB는 객체저장 불가능)
6. OOP의 관점에서 모델링을 할 수 있게 해준다. (상속, 컴포지션, 연관관계)
7. 방언 처리가 용이하여 Migration하기 좋음. 유지보수에도 좋음(mysql, 오라클 등 여러 RDBMS에 사용가능)

# 스프링부트 동작원리
1. 내장 톰켓을 가진다. - 톰켓을 따로 설치할 필요x
2. 서블릿 컨테이너

![image](https://user-images.githubusercontent.com/105253684/203491041-a09b1185-2193-4920-8d6a-924cb29bda00.png)

3. web.xml (웹 배포서술자)
  * ServletContext의 초기 파라미터 생성
  * Session의 유효시간 설정
  * Servlet/JSP에 대한 정의
  * Servlet/JSP에 매핑
  * Mime Type 매핑
  * Welcome File list 설정
  * Error Pages 처리
  * 리스너/필터 설정
  * 보안

</pre>
</details>

<details>
  <summary>00</summary>
<pre>

</pre>
</details>
