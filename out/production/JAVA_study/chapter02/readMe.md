- 변수란?
    - **단 하나의 값을 저장할 수 있는 메모리 공간**
  

- 변수의 선언과 초기화
    - 변수타입
        - 변수에 저장될 값이 어떤 타입인지 지정하는 것
    - 변수이름
        - 변수에 붙인 이름. 메모리 공간에 이름을 붙여주는 것
    - 변수를 선언하면
        - 메모리의 빈 공간에 **변수타입**에 알맞은 크기의 저장공간이 확보되고, 앞으로 이 저장공간은 **변수이름**을 통해 사용할 수 있게 된다
    - int age; //age라는 변수 선언
        - int: 변수타입, age: 변수이름


- 변수의 초기화
    - 변수의 초기화란?
        - 변수를 사용하기 전에 처음으로 값을 지정하는 것
    - 변수 초기화 해야하는 이유
        - 메모리는 여러 프로그램이 공유하는 자원이기 때문에 전에 다른 프로그램에 의해 저장된 쓰레기값이 남아있을 수 있기 때문이다
    - 변수에 값을 저장할 땐 **‘=’** 연산자 이용 (오른쪽의 값을 왼쪽에 저장하라는 뜻)
    - int age = 25; // 변수 age를 선언하고, 25로 초기화
    - 타입이 같은 경우 ,(콤마)를 사용하여 여러 변수를 한 줄에 선언하기도 한다
    - 변수의 종류에 따라 변수의 초기화를 생략할 수 있는 경우도 있지만, 변수는 사용되기 전에 적절한 값으로 초기화 하는 것이 좋다


- 변수 선언 후 대입 값을 선언하는 코드


    class VarEx1 {
    public static void main(String[] args){
    int year = 0;
    int age = 14;
    
            System.out.println(year);
            System.out.println(age);
    
            year = age + 2000;
            age = age + 1;
    
            System.out.println(year);
            System.out.println(age);
        }
    }


- 두 변수의 값을 교환하는 코드


    class VarEx2 {
    public static void main(String[] args){
    int x = 10, y = 20;
    int tmp = 0;
    
            System.out.println("x:" + x + "y:" + y);
    
            tmp = x;
            x = y;
            y = tmp;
    
            System.out.println("x:" + x + "y:" + y);
        }
    }


- 변수의 명명규칙
    - 대소문자가 구분되며 길이에 제한이 없다
    - 예약어를 사용해서는 안 된다
    - 숫자로 시작해서는 안 된다
    - 특수문자는 ‘_’ 와 ‘$’만 허용한다
  

- 변수의 타입

~~~
    기본형(primitive type)
    - 논리형, 문자형, 정수형, 실수형
    계산을 위한 실제 값을 저장한다. 모두 8개
    
    참조형(reference type)
    - 객체의 주소를 저장한다.8개의 기본형을 제외한 나머지 타입.
~~~

- 참조형 변수
    - 변수의 타입으로 클래스의 이름을 사용 → 클래스의 이름이 참조 변수의 타입

    ```java
    클래스이름 변수이름; // 변수의 타입이 기본형이 아닌 것들은 모두 참조변수
    
    Date today = new today(); // Date 객체 생성, 그 주소를 today에 저장
    ```

    - new = 객체를 생성하는 연산자
    - new의 결과는 생성된 객체의 주소
    - 이 주소가 대입연산자에 의해 참조변수 today에 저장되는 것


- 기본형(primitive type)
    - 논리형
        - boolean
            - ture와 false 중 하나를 값으로 갖으며, 조건식과 논리적 계산에 사용
    - 문자형
        - char
            - 문자를 저장하는데 사용되며, 변수에 하나의 문자만 저장할 수 있다
    - 정수형
        - byte, short, int, long
            - 정수를 저장하는데 사용되며, 주로 int가 사용된다. byte는 이진 데이터를 다룰 때 사용되며, short는 c언어와 호완을 위해서 추가되었다.
    - 실수형
        - float, double
            - 실수를 저장하는데 사용되며, 주로 double이 사용된다.


- 상수와 리터럴
    - 상수

      값을 한번만 저장할 수 있는 공간

        - 변수 타입 앞에 키워드 ‘final’을 붙여주기만 하면 된다
        - 상수는 선언과 동시에 초기화해야 하며, 그 후 부터는 상수의 값을 변경할 수 없다

        ```java
        final int MAX_SPEED; // 에러. 상수는 선언과 동시에 초기화해야함
        final int MAX_VALUE = 100; // 가능.
        MAX_VALUE = 200; // 에러. 상수의 값은 변경할 수 없음
        ```

    - 리터럴
        
        그 자체로 값을 의미하는 것
        
        - 프로그래밍에서 상수를 “값을 한 번 저장하면 변경할 수 없는 공간”으로 정의했기 때문에 이와 구분하기 위해 상수를 다른 이름으로 부르는 것
        
    - 상수가 필요한 이유
        - 리터럴에 ‘의미있는 이름’을 붙여서 코드의 이해와 수정을 쉽게 만든다
      

- 리터럴 타입과 접미사

  정수형과 실수형에는 여러 타입이 존재하므로, 리터럴에 접미사를 붙여서 타입을 구분한다

  임시 공간에 데이터를 저장할 때, 접미사를 붙이지 않으면 기본형으로 인식하여 오류가 난다

    - 정수형
        - long 타입 + l (L)
    - 실수형
        - float 타입 + f (F) / doule 타입 + d (D)

- 타입의 불일치
    - 타입이 달라도 저장범위가 넓은 타입에 좁은 아입의 값을 저장하는 것은 허용된다

    ```java
    int i = 'A'; //OK. 유니코드로 변환하여 65가 저장됨.
    long l = 123; //OK. int보다 long타입이 범위가 더 넓다.
    ```

- 문자 리터럴과 문자열 리터럴
    - 문자 리터럴
        - ‘’ 작은 따옴표로 감싸기
        - 하나의 문자 무조건 필요
    - 문자열 리터럴
        - “” 큰 따옴표로 감싸기
        - 내용이 없어도 됨
        - 덧셈 연산자를 통해 문자열을 결합할 수 있음

            ```java
            문자열 + any type -> 문자열 + 문자열 -> 문자열
            any type + 문자열 -> 문자열 + 문자열 -> 문자열
            
            7 + " " -> "7 "
            "" + 7 -> "7"
            7 + 7 + "" -> 14 + "" -> "14" + "" -> "14"
            ```

- 형식화된 출력 printf()
    - 지시자를 통해 변수를 원하는 형식으로 출력할 수 있다
    - 출력 후 줄바꿈을 하지 않기 때문에 줄바꿈을 하려면 %n을 따로 넣어줘야한다
  
    ~~~ java
    System.out.printf("age:%d year:%d", age, year);
    -> System.out.printf("age:%d year:%d", 21, 2023);
    ~~~

    ~~~java
    package chapter02.PrintfEx1;

    class PrintfEx1 {
        public static void main(String[] args){
            byte b = 1;
            short s = 2;
            char c = 'A';

            int finger = 10;
            long big = 100_000_000_000L; // long big = 100000000000
            long hex = 0xFFFF_FFFF_FFFF_FFFFL;

            int octNum = 010;
            int hexNum = 0x10;
            int binNum = 0b10;

            System.out.printf("b=%d%n",b);
            System.out.printf("s=%d%n",s);
            System.out.printf("c=%c, %d %n", c, (int)c);
            System.out.printf("finger=[%5d] %n", finger);
            System.out.printf("finger=[%-5d] %n", finger);
            System.out.printf("finger=[%05d] %n", finger);
            System.out.printf("big=%d %n", big);
            System.out.printf("hex=%#x %n", hex);
            System.out.printf("octNum=%o %d%n", octNum , octNum);
            System.out.printf("hexNum=%x, %d%n", hexNum, hexNum);
            System.out.printf("binNum=%s, %d%n", Integer.toBinaryString(binNum), binNum);
        }
    }
    ~~~

  - ‘ _ ‘ 와 ‘ 0 ‘ 은 여러 값을 여러 줄로 간격 맞춰 출력할 때 사용하는 기능
  - %x 와 %o에 ‘ # ‘ 을 사용하면 접두사 ‘0x’와 ‘0’가 각각 붙는다
  - 10진수를 2진수로 출력해줄 수 없기 때문에 메소드 Integer.toBinaryString(binNum)을 사용한다
    이 메소드는 정수를 2진수로 변환하기 때문에 지시자 %s를 사용한다


- 화면에서 입력받기 Scanner()

  - scanner 클래스를 사용하려면 `import java.util.*;` 를 추가해야 한다.
  - nextLine()이라는 메소드를 호출하면, 입력대기 상태에 있다가 입력을 마치고 '엔터키'를 누르면 입력한 내용이 문자열로 반환된다.
  - 만일 입력받은 문자열을 숫자로 변환하려면 Integer.parserInt() 라는 메소드를 이용해야한다. 이 메소드는 문자열을 int 타입의 정수로 변환한다.
  - 만일 문자열을 float타입의 값으로 변환하길 원하면 Float.parserFloat()를 사용해야한다.
  - Scanner 클래스에는 nextLine() 이나 nextFloat() 같이 변환없이 숫자로 바로 입력받을 수 있는 메소드들이 있고, 이 메소드들을 사용하면 문자열을 숫자로 변환하는 수고는 하지 않아도 된다.

    ~~~java
    int num = scanner.nextLine(); // 정수를 입력받아서 변수 num에 저장
    ~~~

    - 이 메소드들은 화면에서 연속적으로 값을 입력받아서 사용하기에 까다롭다.
    - 차라리 모든 값을 nextLine()으로 입력 받아서 적절히 변환하는 것이 더 낫다.
    

- 기본형
    - 논리형(boolean)
        - boolean형 변수에는 true와 false 중 하나를 저장할 수 있다
        - 기본값은 false
        - boolean형 변수는 주로 대답(yes/no), 스위치(on/off) 등의 논리 구현에 사용된다
        - 크기는 1byte이다
            - true와 false, 두 가지 값만 표현하면 되기 때문에 1bit 로도 충분하지만, 자바에서는 데이터를 다루는 최소 단위가 byte이기 때문
    - 문자형(char)
        - char형의 변수에는 단 하나의 문자만을 저장할 수 있다

        ```java
        char ch = 'A'; //문자 'A'를 char타입의 변수 ch에 저장
        ```

        - 변수에 ‘문자’가 저장되는 것이 아니라 ‘문자의 유니코드’가 저장된다
            - 따라서 문자 리터럴 대신 문자의 유니코드를 직접 저장할 수도 있다

    - 정수형
        - byte, short, int, long 총 4개의 자료형이 존재한다
        - 정수형 변수를 선언할 때는 int타입으로 하고, int의 범위(약 +-20억)를 넘어서는 수를 다뤄야할 때는 long을 사용하면 된다
        - 오버플로우
            - 타입이 표현할 수 있는 값의 범위를 넘어서는 것
            - 오버플로우가 발생했다고 해서 에러가 발생하는 것은 아니다. 단지 예상했던 결과를 얻지 못할 뿐이다

            ```java
            최대값 + 1 -> 최소값
            최소값 - 1 -> 최대값
            ```
            
          -