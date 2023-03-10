## 01. 자바를 시작하기 전에
<br>

### 목차
* 자바란?
* 자바언어의 특징
* 자바로 프로그램 작성하기
* 자주 발생하는 에러와 해결방법
* 자바 프로그램의 실행과정
* 주석

---

- 자바
    - 썬 마이크로시스템즈에서 개발하여 공식적으로 발표한 객체지향 프로그래밍 언어
      <br><br>
- 자바언어의 특징
    - 운영체제에 독립적이다
        - 자바 응용프로그램은 운영체제나 하드웨어가 아닌 JVM하고만 통신한다
        - JVM이 자바 응용프로그램으로부터 전달받은 명령을 해당 운영체제가 이해할 수 있도록 변환하여 전달한다
        - 자바로 작성된 프로그램 → 운영체제에 독립적 , JVM → 운영체제에 종속적( 따라서 각 운영체제에 설치할 수 있는 서로 다른 버전의 JVM 제공)
        - 자바로 작성된 프로그램은 운영체제와 하드웨어에 관계없이 실행 가능하다
          <br><br>
    - 객체지향언어이다
        - 객체지향개념의 특징인 상속, 캡슐화, 다형성이 잘 적용된 순수한 객체지향 언어이다
          <br><br>
    - 비교적 배우기 쉽다
        - 연산자, 기본구문 → C++ , 객체지향관련 구문 → small talk
          <br>
          ⇒ 장점은 취하고, 단순화함으로서 쉽게 배울 수 있으며, 간결하고 이해하기 쉬운 코드를 작성할 수 있도록 하였다
          <br><br>
    - 자동 메모리 관리(Garbage Collection)
        - 자바로 작성된 프로그램 실행 → 가비지컬렉터 자동 실행
          <br>
          ⇒ 프로그래머가 따로 메모리 관리를 하지 않아도 된다
          <br>
        - 자동으로 관리한다는 것이 비효율적인 면도 있지만, 프로그래밍에 집중할 수 있게 도와준다
          <br><br>
    - 네트워크와 분산처리를 지원한다
        - 다양한 네트워크 프로그래밍 라이브러리(Java API)를 통해 비교적 짧은 시간에 네트워크 관련 프로그램을 쉽게 개발할 수 있도록 지원한다
          <br><br>
    - 멀티쓰레드를 지원한다
        - 자바에서 개발되는 멀티쓰에드 프로그램은 시스템과는 관계없이 구현가능하며, 관련된 라이브러리(Java API)가 제공되므로 구현이 쉽다.
        - 여러 쓰레드에 대한 스케줄링을 자바 인터프린터가 담당하게 된다
          <br><br>
    - 동적 로딩(Dynamic Loading)을 지원한다
        - 실행 시에 모든 클래스가 로딩되지 않고 필요한 시점에 클래스를 로딩하여 사용할 수 있다
        - 일부 클래스가 변경되어도 전체 애플리케이션을 다시 컴파일하지 않아도 된다
        - 애플리케이션의 변경사항이 발생해도 비교적 적은 작업만으로도 처리할 수 있는 유연한 애플리케이션을 작성할 수 있다
          <br><br>
    - 속도 문제
        - 바이트코드를 하드웨어의 기계어로 바로 변환해주는 JIT컴파일러와 Hotspot과 같은 신기술의 도입 → JVM 기능 향상 ⇒ 속도문제 개선
          <br><br>

- 자바로 프로그램 작성하기
    - 모든 코드는 클래스 안에 존재해야 하며, 서로 관련돤 코드들을 그룹으로 나누어 별도의 클래스 구성
      <br> ⇒ 클래스들이 모여 하나의 Java 애플리케이션을 이룸
      <br><br>

    - 클래스를 작성하는 방법
      <br>
      :키워드 ‘class’ 다음에 클래스의 이름 작성 → 괄호 {} 안에 원하는 코드 작성

        - ‘public static void main (String[] args)’는 main메소드의 선언부
          <br>
          ⇒ 프로그램을 실행할 때 ‘java.exe’에 의해 호출될 수 있도록 미리 약속된 부분이므로 항상 적어줘야 한다

```java
 class 클래스이름{
    public static void main (String[] args) //main메소드의 선언부
    {
        //실행될 코드
    }
}
 ```

- main 메소드
    - 하나의 Java 애플리케이션에는 main 메소드를 포함한 클래스가 반드시 하나는 있어야 한다
    - main 메소드는 Java애플리케이션의 시작점이므로 main 메소드 없이는 실행될 수 없다
    - 작성된 Java애플리케이션을 실행할 때는 ‘java.exe’ 다음에 main메소드를 포함한 클래스의 이름을 적어줘야 한다
      <br><br>
- 소스파일
    - 하나의 소스파일에 하나의 클래스만을 정의하는 것이 보통이지만, 하나의 소스파일에 둘 이상의 클래스를 정의하는 것도 가능하다
    - 주의할 점은 ‘소스파일의 이름은 public class의 이름과 일치해야 한다’는 것이다
    - 소스파일 내에 public class가 없다면 소스파일 이름은 소스파일 내의 어떤 클래스의 이름으로 해도 상관없다
      <br><br>

- 자주 발생하는 에러와 해결방법
  <br>
    - cannot find symbol OR cannot resolve symbol
      <br>
      지정된 변수나 메소드를 찾을 수 없다는 뜻. 철자와 대소문자의 일치여부까지 확인해야 한다.
      <br><br>
    - ‘;’ expected
      <br>
      세미콜론이 필요한 곳에 없다는 뜻. 모든 문장의 끝에는 세미콜론을 붙여주어야 한다.
      <br><br>
    - Exception in thread “main” java.lang.NoSuchMethodError: main
      <br>
      main 메소드를 찾을 수 없다는 뜻. main메소드가 존재하지 않거나 선언부 ‘public static void main (String[] args)’에 오타가 존재하는 경우에 발생한다.
      <br><br>
    - Exception in thread “main” java.lang.NoClassDefFoundError: Hello
      <br>
      Hello라는 클래스를 찾을 수 없다는 뜻. 클래스의 철자와 대소문자를 확인해보고 이상이 없으면 클래스파일(.class)이 생성 되었는지 확인한다.
      <br><br>
    - illegal start of expression
      <br>
      문장에 문법적인 오류가 있다는 뜻. 괄호를 열고 닫지 않거나, 수식이나 if문, for문 등에 문법적 오류가 있을 때 또는 public이나 static 같은 키워드를 잘못 사용한 경우에도 발생한다.
      <br><br>
    - class, interface, or enum expected
      <br>
      키워드 class나 interface 또는 enum이 없다는 뜻. 하지만 보통 괄호의 개수가 일치하지 않는 경우에 발생한다.
      <br><br>

- 주석
    - 프로그램 코드에 대한 설명을 적절히 덧붙여 놓기 위하여 사용한다
    - 프로그램의 작성자, 작성일시, 버전과 그에 따른 변경이력 등의 정보를 제공할 목적으로도 사용된다

    ```
    범위 주석: '/*' 와 '*/' 사이의 내용은 주석으로 간주된다
    한 줄 주석: '//'부터 라인 끝까지의 내용은 주석으로 간주된다
    ```