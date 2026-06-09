202530124이채원

---

# 0318 강의

## 1. 절차 지향 언어

절차 지향 언어는 프로그램을 **순서와 절차에 따라 실행**하는 방식이다.

### 특징

* 데이터와 함수를 분리해서 사용한다.
* 실행 순서가 중요하다.
* 전역 변수를 많이 사용하는 경우가 많다.
* 코드 재사용과 유지보수가 어렵다.
* 코드 유연성이 부족할 수 있다.

### 대표 언어

```text
C, Pascal, Fortran
```

---

## 2. 객체 지향 언어

객체 지향 언어는 현실 세계의 객체를 프로그램으로 모델링하는 방식이다.

객체는 **데이터와 메소드**를 함께 가진다.

### 특징

* 객체 중심으로 프로그램을 작성한다.
* 데이터와 메소드를 하나로 묶는다.
* 코드 재사용성이 높다.
* 유지보수가 쉽다.
* 상속, 캡슐화, 다형성을 활용한다.

### 대표 언어

```text
Java, C++, Python
```

---

## 3. 함수 지향 언어

함수 지향 언어는 함수를 중심으로 프로그램을 작성하는 방식이다.

### 특징

* 함수를 일급 객체로 취급한다.
* 상태 변경을 피하고 불변성을 지향한다.
* 함수 조합으로 복잡한 작업을 수행한다.
* 재귀, 고차 함수, 순수 함수를 중요하게 다룬다.
* 병렬 처리와 추상화에 유리하다.

### 대표 언어

```text
Python, Kotlin, Haskell, Lisp, Scala
```

---

## 4. 자바의 플랫폼 독립성

### WORA

```text
Write Once Run Anywhere
```

뜻은 **한 번 작성한 코드는 어느 플랫폼에서나 실행할 수 있다**는 의미이다.

자바는 운영체제나 하드웨어에 직접 종속되지 않고, JVM 위에서 실행된다.

---

## 5. 바이트 코드와 JVM

### 바이트 코드

바이트 코드는 자바 소스를 컴파일한 결과물이다.

```text
.java 파일 → 컴파일 → .class 파일
```

### 특징

* CPU에 종속되지 않는다.
* 운영체제에 직접 종속되지 않는다.
* JVM에 의해 실행된다.

### JVM

JVM은 **Java Virtual Machine**의 약자이다.

JVM은 자바 바이트 코드를 실행하는 소프트웨어이다.

```text
자바 코드가 플랫폼 독립성을 가지는 이유 = 바이트 코드 + JVM
```

---

# 0325 강의

## 1. 자바의 특징

### 가비지 컬렉션

자바는 개발자가 직접 메모리를 반환하지 않는다.

사용하지 않는 메모리는 JVM이 자동으로 회수한다.

```text
가비지 컬렉션 = JVM이 사용하지 않는 객체 메모리를 자동으로 회수하는 기능
```

---

## 2. 주석

### 한 줄 주석

```java
// 한 줄 주석
```

### 여러 줄 주석

```java
/*
여러 줄 주석
*/
```

---

## 3. 상수

상수는 실행 중 값이 변하지 않는 값이다.

자바에서는 `final` 키워드를 사용한다.

```java
final double PI = 3.141592;
```

### 특징

* 선언할 때 초기값을 지정해야 한다.
* 실행 중 값을 변경할 수 없다.

---

## 4. 변수

변수는 프로그램 실행 중 값을 임시로 저장하는 공간이다.

```java
int age = 20;
double height = 175.5;
```

---

## 5. 자바의 데이터 타입

자바의 데이터 타입은 크게 두 가지이다.

```text
1. 기본 타입
2. 레퍼런스 타입
```

### 기본 타입 8개

```text
boolean, char, byte, short, int, long, float, double
```

### 레퍼런스 타입

객체를 참조하는 타입이다.

예시는 다음과 같다.

```text
String, 배열, 클래스, 인터페이스
```

---

## 6. 문자열

자바에서 문자열은 기본 타입이 아니라 `String` 클래스이다.

```java
String name = "Java";
```

문자열 비교는 `==`보다 `equals()`를 사용한다.

```java
String a = "Java";
String b = "Java";

System.out.println(a.equals(b));
```

---

## 7. 타입 변환

### 자동 타입 변환

작은 타입이 큰 타입으로 자동 변환된다.

```java
long a = 10;
double b = 10;
```

### 강제 타입 변환

개발자가 직접 타입을 바꾸는 것이다.

```java
double d = 3.14;
int n = (int)d;
```

값 손실이 발생할 수 있다.

---

## 8. Scanner

`Scanner`는 키보드 입력을 쉽게 받기 위한 클래스이다.

```java
import java.util.Scanner;

Scanner sc = new Scanner(System.in);

int age = sc.nextInt();
String name = sc.next();
```

---

## 9. 연산자

### 산술 연산자

```text
+  -  *  /  %
```

### 증감 연산자

```text
++  --
```

### 전위 증가

```java
int a = 1;
int b = ++a;

// a = 2, b = 2
```

### 후위 증가

```java
int a = 1;
int b = a++;

// a = 2, b = 1
```

### 비교 연산자

```text
<, >, <=, >=, ==, !=
```

### 논리 연산자

```text
!, &&, ||, ^
```

---

# 0401 강의

## 1. 조건문

### if문

```java
if(조건식) {
    실행문;
}
```

### if-else문

```java
if(조건식) {
    실행문1;
} else {
    실행문2;
}
```

### else-if문

```java
if(조건식1) {
    실행문1;
} else if(조건식2) {
    실행문2;
} else {
    실행문3;
}
```

---

## 2. switch문

하나의 값과 여러 case 값을 비교할 때 사용한다.

```java
switch(변수) {
    case 값1:
        실행문;
        break;
    case 값2:
        실행문;
        break;
    default:
        실행문;
}
```

### 주의점

```text
break가 없으면 다음 case까지 계속 실행된다.
```

switch문에는 정수, 문자, 문자열을 사용할 수 있다.

---

## 3. 반복문

### for문

반복 횟수가 명확할 때 사용한다.

```java
for(int i = 0; i < 5; i++) {
    System.out.println(i);
}
```

### while문

조건이 참인 동안 반복한다.

```java
while(조건식) {
    실행문;
}
```

### do-while문

최소 한 번은 실행한다.

```java
do {
    실행문;
} while(조건식);
```

---

## 4. break와 continue

### break

반복문을 즉시 종료한다.

```java
for(int i = 0; i < 10; i++) {
    if(i == 5) break;
}
```

### continue

현재 반복을 건너뛰고 다음 반복으로 넘어간다.

```java
for(int i = 0; i < 10; i++) {
    if(i == 5) continue;
    System.out.println(i);
}
```

---

## 5. 배열

배열은 같은 타입의 데이터를 연속적으로 저장하는 자료구조이다.

### 특징

* 같은 타입만 저장 가능하다.
* 인덱스는 0부터 시작한다.
* 반복문과 함께 사용하기 좋다.
* 생성 후 크기 변경이 어렵다.

---

## 6. 배열 선언과 생성

### 선언

```java
int[] arr;
```

또는

```java
int arr[];
```

### 생성

```java
arr = new int[5];
```

### 선언과 생성 동시에 하기

```java
int[] arr = new int[5];
```

### 초기화

```java
int[] arr = {1, 2, 3};
```

---

## 7. 배열 인덱스

크기가 5인 배열의 인덱스 범위는 다음과 같다.

```text
0 ~ 4
```

잘못된 예시:

```java
int[] arr = new int[5];

arr[-1] = 10; // 오류
arr[5] = 10;  // 오류
```

---

## 8. length 필드

배열의 크기는 `length`로 확인한다.

```java
int[] arr = new int[5];

System.out.println(arr.length);
```

배열 전체 출력:

```java
for(int i = 0; i < arr.length; i++) {
    System.out.println(arr[i]);
}
```

---

## 9. for-each문

배열의 모든 원소를 순서대로 접근할 때 사용한다.

```java
int[] arr = {1, 2, 3, 4, 5};

for(int n : arr) {
    System.out.println(n);
}
```

---

## 10. 2차원 배열

2차원 배열은 행과 열로 구성된다.

```java
int[][] arr = new int[2][5];
```

초기화:

```java
int[][] arr = {
    {0, 1, 2},
    {3, 4, 5},
    {6, 7, 8}
};
```

길이 확인:

```java
arr.length     // 행의 개수
arr[0].length  // 0번째 행의 열 개수
```

---

## 11. 배열 레퍼런스

배열 변수끼리 대입하면 배열이 복사되는 것이 아니라 같은 배열을 공유한다.

```java
int[] a = new int[5];
int[] b = a;

a[0] = 10;

System.out.println(b[0]); // 10
```

---

## 12. 비트 연산

비트 연산은 데이터를 비트 단위로 처리하는 연산이다.

### 비트 논리 연산

```text
AND: &
OR : |
XOR: ^
NOT: ~
```

### 비트 시프트 연산

```text
<<, >>
```

예시:

```java
int x = 5;
int result = x << 1;

System.out.println(result); // 10
```

비트 연산은 빠른 연산, 플래그 처리, 권한 설정, 최적화 등에 사용된다.

---

# 0408 강의

## 1. 클래스

클래스는 객체를 만들기 위한 설계도이다.

```java
class Circle {
    int radius;

    double getArea() {
        return radius * radius * 3.14;
    }
}
```

---

## 2. 객체

객체는 클래스를 이용해 실제로 생성된 실체이다.

```java
Circle pizza = new Circle();
```

객체는 인스턴스라고도 부른다.

---

## 3. 클래스 구성

클래스는 필드와 메소드로 구성된다.

```java
class Student {
    String name;

    void study() {
        System.out.println("공부합니다.");
    }
}
```

```text
필드 = 객체의 데이터
메소드 = 객체의 동작
```

---

## 4. 객체 지향 프로그래밍

객체 지향 프로그래밍은 객체들 사이의 상호작용으로 프로그램을 작성하는 방식이다.

### 장점

* 코드 재사용이 쉽다.
* 유지보수가 쉽다.
* 실세계를 모델링하기 쉽다.
* 프로그램 확장이 쉽다.

---

## 5. 캡슐화

캡슐화는 객체의 내부 데이터를 외부에서 함부로 접근하지 못하게 보호하는 것이다.

```text
캡슐화 = 데이터 보호
```

---

## 6. 상속

상속은 상위 클래스의 멤버를 하위 클래스가 물려받는 것이다.

```java
class Animal {
    String name;

    void eat() {
        System.out.println("먹는다");
    }
}

class Human extends Animal {
    String job;

    void work() {
        System.out.println("일한다");
    }
}
```

```text
상위 클래스 = 슈퍼 클래스
하위 클래스 = 서브 클래스
```

---

## 7. 다형성

다형성은 같은 이름의 메소드가 객체에 따라 다르게 동작하는 것이다.

대표적인 예시는 다음과 같다.

```text
1. 메소드 오버로딩
2. 메소드 오버라이딩
```

---

## 8. 예외 처리

예외는 프로그램 실행 중 발생하는 예상치 못한 오류이다.

예외 발생 예시:

```text
0으로 나누기
배열 범위 초과
숫자 입력 자리에 문자 입력
```

예외 처리는 `try-catch-finally`문을 사용한다.

```java
try {
    예외가 발생할 수 있는 코드
} catch(Exception e) {
    예외 처리 코드
} finally {
    무조건 실행되는 코드
}
```

`finally`는 생략 가능하다.

---

# 0415 강의

## 1. 생성자

생성자는 객체가 생성될 때 자동으로 호출되는 메소드이다.

객체 초기화를 위해 사용한다.

```java
class Circle {
    int radius;

    public Circle() {
        radius = 1;
    }
}
```

---

## 2. 생성자의 특징

```text
생성자 이름은 클래스 이름과 같다.
리턴 타입이 없다.
객체 생성 시 한 번만 호출된다.
new 연산자로 객체를 생성할 때 호출된다.
여러 개 작성할 수 있다.
초기화 목적으로 사용된다.
```

---

## 3. 생성자 중복

생성자는 매개변수의 개수나 타입을 다르게 해서 여러 개 만들 수 있다.

```java
class Circle {
    int radius;
    String name;

    public Circle() {
        radius = 1;
    }

    public Circle(int r, String n) {
        radius = r;
        name = n;
    }
}
```

---

## 4. 기본 생성자

기본 생성자는 매개변수가 없는 생성자이다.

```java
class Circle {
    public Circle() {
    }
}
```

클래스에 생성자가 하나도 없으면 컴파일러가 기본 생성자를 자동으로 만든다.

하지만 생성자를 하나라도 직접 작성하면 기본 생성자는 자동 생성되지 않는다.

---

## 5. this

`this`는 객체 자기 자신을 가리킨다.

```java
class Circle {
    int radius;

    public Circle(int radius) {
        this.radius = radius;
    }
}
```

필드 이름과 매개변수 이름이 같을 때 자주 사용한다.

---

## 6. this()

`this()`는 같은 클래스의 다른 생성자를 호출할 때 사용한다.

```java
public Book() {
    this("", "", 0);
}
```

주의점:

```text
생성자 안에서만 사용 가능
반드시 생성자의 첫 번째 문장이어야 함
```

잘못된 예시:

```java
public Book() {
    System.out.println("생성자 호출");
    this("", "", 0); // 오류
}
```

---

## 7. 객체 배열

객체 배열은 객체 자체를 저장하는 것이 아니라 객체의 레퍼런스를 저장하는 배열이다.

### 객체 배열 생성 3단계

```text
1. 배열 레퍼런스 변수 선언
2. 레퍼런스 배열 생성
3. 배열의 각 원소 객체 생성
```

예시:

```java
Circle[] c;
c = new Circle[5];

for(int i = 0; i < c.length; i++) {
    c[i] = new Circle(i);
}
```

---

## 8. 메소드

메소드는 클래스 안에 작성되는 함수이다.

```java
public int getSum(int i, int j) {
    int sum = i + j;
    return sum;
}
```

메소드 구성:

```text
접근 지정자
리턴 타입
메소드 이름
매개변수
메소드 코드
```

---

## 9. 메소드 오버로딩

오버로딩은 같은 이름의 메소드를 여러 개 작성하는 것이다.

조건:

```text
메소드 이름이 같아야 한다.
매개변수 개수나 타입이 달라야 한다.
리턴 타입만 다른 것은 오버로딩이 아니다.
```

예시:

```java
public int getSum(int i, int j) {
    return i + j;
}

public int getSum(int i, int j, int k) {
    return i + j + k;
}

public double getSum(double i, double j) {
    return i + j;
}
```

---

## 10. 인자 전달

### 기본 타입 전달

값이 복사되어 전달된다.

메소드 안에서 값을 바꿔도 원래 값은 바뀌지 않는다.

### 배열 전달

배열의 레퍼런스가 전달된다.

메소드 안에서 배열 값을 바꾸면 원래 배열도 바뀐다.

### 객체 전달

객체의 레퍼런스가 전달된다.

메소드 안에서 객체의 필드를 바꾸면 원래 객체도 바뀐다.

---

## 11. 가비지

가비지는 가리키는 레퍼런스가 하나도 없는 객체이다.

```text
가비지 = 더 이상 접근할 수 없는 객체
```

---

## 12. 가비지 컬렉션

가비지 컬렉션은 JVM이 가비지를 자동으로 회수하는 기능이다.

```java
System.gc();
```

위 코드는 가비지 컬렉션을 요청하는 코드이다.

하지만 실제 실행 시점은 JVM이 결정한다.

---

## 13. 접근 지정자

자바의 접근 지정자는 4가지이다.

```text
private
default
protected
public
```

| 접근 지정자    | 접근 범위            |
| --------- | ---------------- |
| private   | 같은 클래스 안에서만      |
| default   | 같은 패키지 안에서만      |
| protected | 같은 패키지 또는 서브 클래스 |
| public    | 모든 클래스           |

---

## 14. static

`static` 멤버는 클래스당 하나만 생성된다.

객체들이 함께 공유한다.

```java
class StaticSample {
    int n;
    static int m;
}
```

사용 예시:

```java
StaticSample.m = 10;
```

### static 특징

```text
클래스 이름으로 접근 가능
객체들이 공유
static 메소드는 static 멤버만 직접 접근 가능
this 사용 불가
```

---

## 15. final

### final 필드

상수를 만들 때 사용한다.

```java
public static final double PI = 3.14;
```

### final 클래스

상속할 수 없다.

```java
final class MyClass {
}
```

### final 메소드

오버라이딩할 수 없다.

```java
final void print() {
}
```

---

# 0429 강의

## 1. 상속

상속은 부모 클래스의 멤버를 자식 클래스가 물려받는 것이다.

```java
class Person {
    String name;
}

class Student extends Person {
    String grade;
}
```

상속에는 `extends` 키워드를 사용한다.

```text
부모 클래스 = 슈퍼 클래스
자식 클래스 = 서브 클래스
```

---

## 2. 자바 상속 특징

```text
클래스 다중 상속 불가
인터페이스 다중 구현 가능
모든 클래스는 Object 클래스를 자동 상속
서브 클래스 객체는 슈퍼 클래스 멤버를 포함
```

---

## 3. 슈퍼 클래스 멤버 접근

```text
private   : 서브 클래스에서 접근 불가
default   : 같은 패키지에서 접근 가능
protected : 같은 패키지 또는 서브 클래스에서 접근 가능
public    : 항상 접근 가능
```

---

## 4. super()

`super()`는 서브 클래스 생성자에서 슈퍼 클래스 생성자를 호출할 때 사용한다.

서브 클래스 객체가 생성될 때는 다음 생성자가 실행된다.

```text
슈퍼 클래스 생성자 1개
서브 클래스 생성자 1개
```

---

## 5. 업캐스팅

업캐스팅은 서브 클래스 객체를 슈퍼 클래스 타입으로 다루는 것이다.

```java
class Person { }
class Student extends Person { }

Student s = new Student();
Person p = s;
```

---

## 6. 다운캐스팅

다운캐스팅은 업캐스팅된 객체를 다시 서브 클래스 타입으로 변환하는 것이다.

```java
Person p = new Student();
Student s = (Student)p;
```

다운캐스팅은 명시적 형변환이 필요하다.

---

## 7. instanceof

`instanceof`는 객체의 실제 타입을 확인하는 연산자이다.

결과는 `true` 또는 `false`이다.

```java
if(p instanceof Student) {
    Student s = (Student)p;
}
```

---

## 8. 메소드 오버라이딩

오버라이딩은 서브 클래스에서 슈퍼 클래스의 메소드를 다시 작성하는 것이다.

```java
class Animal {
    void sound() {
        System.out.println("소리");
    }
}

class Dog extends Animal {
    void sound() {
        System.out.println("멍멍");
    }
}
```

### 오버라이딩 조건

```text
메소드 이름이 같아야 한다.
매개변수 타입과 개수가 같아야 한다.
리턴 타입이 같아야 한다.
상속 관계여야 한다.
```

---

## 9. 오버로딩과 오버라이딩 비교

| 구분     | 오버로딩            | 오버라이딩 |
| ------ | --------------- | ----- |
| 관계     | 같은 클래스 또는 상속 관계 | 상속 관계 |
| 메소드 이름 | 같음              | 같음    |
| 매개변수   | 달라야 함           | 같아야 함 |
| 리턴 타입  | 상관없음            | 같아야 함 |
| 목적     | 편리성             | 다형성   |

---

## 10. 추상 클래스

추상 클래스는 `abstract`로 선언된 클래스이다.

```java
abstract class Shape {
    abstract public void draw();
}
```

### 특징

```text
객체를 직접 생성할 수 없다.
상속을 위한 슈퍼 클래스로 사용된다.
서브 클래스에서 추상 메소드를 구현해야 한다.
```

---

## 11. 추상 메소드

추상 메소드는 코드 없이 원형만 선언된 메소드이다.

```java
abstract public void draw();
```

---

## 12. 인터페이스

인터페이스는 클래스가 구현해야 할 규격이다.

```java
interface PhoneInterface {
    public static final int TIMEOUT = 10000;
    public abstract void sendCall();
}
```

### 인터페이스 구성 요소

```text
상수
추상 메소드
default 메소드
private 메소드
```

인터페이스에서 상수는 `public static final`을 생략할 수 있다.

추상 메소드는 `public abstract`를 생략할 수 있다.

---

## 13. 패키지

패키지는 관련 있는 클래스와 인터페이스를 묶어 놓은 디렉터리이다.

```java
package com.company.project;
```

### 목적

```text
클래스 관리
이름 충돌 방지
프로그램 구조화
```

패키지 이름은 보통 도메인 기반으로 작성한다.

```text
com.회사이름.프로젝트명.기능
```

---

## 14. 모듈

모듈은 여러 패키지와 자원을 모아 놓은 컨테이너이다.

Java 9부터 모듈화가 도입되었다.

### 목적

```text
Java API를 여러 모듈로 분리
필요한 모듈만 사용
작은 실행 환경 구성 가능
```

---

# 0506 강의

## 1. Object 클래스

모든 자바 클래스는 자동으로 `Object` 클래스를 상속받는다.

```text
Object 클래스 = 모든 클래스의 최상위 클래스
```

---

## 2. 주요 패키지

| 패키지         | 설명               |
| ----------- | ---------------- |
| java.lang   | 기본 클래스 제공        |
| java.util   | 유틸리티 클래스 제공      |
| java.io     | 입출력 클래스 제공       |
| java.awt    | AWT GUI 클래스 제공   |
| javax.swing | Swing GUI 클래스 제공 |

### java.lang

자동으로 import 된다.

예시:

```text
String, Math, Object
```

### java.util

예시:

```text
Scanner, ArrayList, HashMap
```

---

## 3. Wrapper 클래스

Wrapper 클래스는 기본 타입을 객체로 감싸는 클래스이다.

| 기본 타입   | Wrapper 클래스 |
| ------- | ----------- |
| int     | Integer     |
| char    | Character   |
| double  | Double      |
| boolean | Boolean     |
| byte    | Byte        |
| short   | Short       |
| long    | Long        |
| float   | Float       |

컬렉션은 객체만 저장할 수 있기 때문에 기본 타입을 Wrapper 클래스로 감싸서 사용한다.

---

## 4. 박싱과 언박싱

### 박싱

기본 타입을 Wrapper 객체로 변환하는 것이다.

```java
Integer i = Integer.valueOf(10);
```

### 언박싱

Wrapper 객체에서 기본 타입 값을 꺼내는 것이다.

```java
int n = i.intValue();
```

### 자동 박싱과 자동 언박싱

JDK 1.5부터 자동으로 처리된다.

```java
Integer i = 10;
int n = i;
```

---

## 5. String 활용

문자열 비교는 `equals()`를 사용한다.

```java
String a = "Java";
String b = "Java";

System.out.println(a.equals(b));
```

`==`는 문자열 내용 비교가 아니라 레퍼런스 비교가 될 수 있으므로 주의해야 한다.

공백 제거는 `trim()`을 사용한다.

```java
String s = " Java ";
System.out.println(s.trim());
```

---

## 6. StringBuffer

`StringBuffer`는 변경 가능한 문자열을 다루는 클래스이다.

```java
StringBuffer sb = new StringBuffer("Java");
```

### 특징

```text
문자열 수정 가능
가변 크기 버퍼 사용
문자열 변경이 많은 작업에 적합
```

---

## 7. Math 클래스

Math 클래스는 수학 연산 메소드를 제공한다.

모든 메소드는 static이다.

```java
Math.random();
Math.sqrt(4);
Math.max(10, 20);
```

객체를 만들지 않고 클래스 이름으로 호출한다.

---

## 8. 컬렉션

컬렉션은 가변 개수의 객체를 저장하는 저장소이다.

### 특징

```text
객체 저장 가능
크기 자동 조절
삽입, 삭제, 검색 편리
배열보다 유연함
```

---

## 9. 제네릭

제네릭은 클래스나 메소드에서 사용할 타입을 일반화하는 기법이다.

```java
ArrayList<String> list = new ArrayList<String>();
```

### 장점

```text
타입 안정성 증가
불필요한 형변환 감소
여러 타입에 재사용 가능
```

---

## 10. ArrayList

ArrayList는 가변 크기 배열을 구현한 클래스이다.

```java
import java.util.ArrayList;

ArrayList<String> list = new ArrayList<String>();

list.add("Java");
list.add("Python");

System.out.println(list.get(0));
```

### 특징

```text
크기 자동 증가
삽입, 삭제, 검색 가능
Vector와 비슷함
스레드 동기화 기능 없음
```

---

## 11. HashMap

HashMap은 key-value 구조로 데이터를 저장한다.

```java
import java.util.HashMap;

HashMap<String, Integer> map = new HashMap<String, Integer>();

map.put("apple", 1000);
map.put("banana", 2000);

System.out.println(map.get("apple"));
```

```text
K = Key
V = Value
```

---

# 0520 강의

## 1. 이벤트 기반 프로그래밍

이벤트 기반 프로그래밍은 이벤트 발생에 따라 프로그램 흐름이 결정되는 방식이다.

예를 들어 사용자가 버튼을 클릭하면 버튼 클릭 이벤트를 처리하는 코드가 실행된다.

```text
이벤트 발생 → 이벤트 객체 생성 → 리스너 호출 → 이벤트 처리
```

---

## 2. 이벤트 종류

```text
마우스 클릭
마우스 드래그
키보드 입력
버튼 클릭
체크박스 선택
네트워크 데이터 수신
다른 스레드의 메시지
```

GUI 프로그램은 대부분 이벤트 기반 프로그래밍으로 작성된다.

---

## 3. 이벤트 리스너

이벤트 리스너는 이벤트가 발생했을 때 실행되는 코드이다.

대표적인 리스너는 다음과 같다.

```text
ActionListener
MouseListener
KeyListener
ItemListener
```

---

## 4. ActionListener

ActionListener는 버튼 클릭 같은 Action 이벤트를 처리한다.

```java
interface ActionListener {
    public void actionPerformed(ActionEvent e);
}
```

예시:

```java
class MyActionListener implements ActionListener {
    public void actionPerformed(ActionEvent e) {
        JButton b = (JButton)e.getSource();

        if(b.getText().equals("Action"))
            b.setText("액션");
        else
            b.setText("Action");
    }
}
```

---

## 5. 이벤트 리스너 작성 과정

```text
1. 처리할 이벤트와 리스너 선택
2. 리스너 인터페이스를 구현한 클래스 작성
3. 이벤트 처리 메소드 구현
4. 컴포넌트에 리스너 등록
```

리스너 등록 형식:

```java
component.addXXXListener(listener);
```

예시:

```java
MyActionListener listener = new MyActionListener();
btn.addActionListener(listener);
```

---

## 6. 이벤트 객체

이벤트 객체는 발생한 이벤트에 대한 정보를 담고 있는 객체이다.

### 포함 정보

```text
이벤트 종류
이벤트 소스
이벤트 발생 좌표
버튼이나 메뉴 아이템 문자열
마우스 버튼 번호
마우스 클릭 횟수
키 코드 값과 문자 값
체크 상태
```

---

## 7. getSource()

`getSource()`는 이벤트가 발생한 컴포넌트를 알려준다.

```java
Object obj = e.getSource();
```

Object 타입으로 리턴되므로 캐스팅해서 사용한다.

```java
JButton b = (JButton)e.getSource();
```

---

## 8. 이벤트 리스너 작성 방법 3가지

### 1. 독립 클래스

리스너를 별도의 클래스로 작성한다.

여러 곳에서 사용할 때 적합하다.

### 2. 내부 클래스

클래스 안에 리스너 클래스를 작성한다.

특정 클래스에서만 사용할 때 적합하다.

### 3. 익명 클래스

클래스 이름 없이 간단히 작성한다.

간단한 리스너에 적합하다.

---

## 9. 익명 클래스

익명 클래스는 이름 없는 클래스이다.

클래스 선언과 객체 생성을 동시에 한다.

```java
btn.addActionListener(new ActionListener() {
    public void actionPerformed(ActionEvent e) {
        System.out.println("버튼 클릭");
    }
});
```

---

## 10. EDT

EDT는 **Event Dispatch Thread**의 약자이다.

Swing GUI 프로그램이 실행될 때 JVM이 자동으로 생성하는 스레드이다.

### 역할

```text
프레임 화면 그리기
컴포넌트 위치와 크기 조절
마우스 클릭 처리
키보드 입력 처리
GUI 이벤트 처리
```

---

## 11. Swing 단일 스레드 모델

Swing 컴포넌트는 멀티스레드에 안전하지 않다.

따라서 GUI 생성과 변경은 EDT에서 처리하는 것이 권장된다.

```java
public static void main(String[] args) {
    javax.swing.SwingUtilities.invokeLater(() -> {
        new MyFrame();
    });
}
```

---

# 시험 핵심 암기

## 1. WORA

```text
Write Once Run Anywhere
한 번 작성한 코드는 JVM이 있는 모든 환경에서 실행 가능
```

---

## 2. 바이트 코드

```text
자바 소스를 컴파일한 .class 코드
CPU에 종속되지 않음
JVM이 실행함
```

---

## 3. 생성자

```text
클래스 이름과 같음
리턴 타입 없음
객체 생성 시 자동 호출
초기화 목적
여러 개 작성 가능
```

---

## 4. this와 this()

```text
this   = 객체 자기 자신
this() = 같은 클래스의 다른 생성자 호출
```

```text
this()는 생성자의 첫 번째 문장이어야 함
```

---

## 5. 배열

```text
인덱스는 0부터 시작
범위는 0 ~ length-1
생성 전에 접근하면 오류
배열 변수끼리 대입하면 같은 배열 공유
```

---

## 6. 오버로딩과 오버라이딩

```text
오버로딩 = 같은 이름, 다른 매개변수
오버라이딩 = 부모 메소드를 자식 클래스에서 재정의
```

---

## 7. static

```text
클래스당 하나만 생성
객체들이 공유
클래스 이름으로 접근 가능
this 사용 불가
```

---

## 8. final

```text
final 필드 = 상수
final 클래스 = 상속 불가
final 메소드 = 오버라이딩 불가
```

---

## 9. 상속

```text
extends 사용
부모 클래스 = 슈퍼 클래스
자식 클래스 = 서브 클래스
자바는 클래스 다중 상속 불가
모든 클래스는 Object 상속
```

---

## 10. 업캐스팅과 다운캐스팅

```text
업캐스팅 = 자식 객체를 부모 타입으로 다룸
다운캐스팅 = 부모 타입을 다시 자식 타입으로 변환
```

```java
Person p = new Student();
Student s = (Student)p;
```

---

## 11. instanceof

```text
객체의 실제 타입을 확인
결과는 true 또는 false
```

---

## 12. 추상 클래스와 인터페이스

```text
추상 클래스 = abstract 클래스, 객체 생성 불가
인터페이스 = 클래스가 구현해야 할 규격
```

---

## 13. 컬렉션

```text
컬렉션 = 가변 개수의 객체 저장소
ArrayList = 가변 크기 배열
HashMap = key-value 저장
```

---

## 14. 이벤트 처리

```text
이벤트 발생
이벤트 객체 생성
리스너 호출
이벤트 처리 코드 실행
```

---

## 15. 이벤트 리스너 등록

```java
component.addXXXListener(listener);
```

---

## 16. getSource()

```text
이벤트가 발생한 컴포넌트를 리턴
Object 타입으로 리턴하므로 캐스팅 필요
```

---

## 17. EDT

```text
Event Dispatch Thread
Swing GUI 이벤트 처리 스레드
GUI 생성과 변경은 EDT에서 처리하는 것이 권장됨
```
