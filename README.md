# 🏄‍♂️java-next-it(이것이 자바다-신용권)

## 📚1.1 프로그래밍 언어란?

- 컴퓨터가 이해할 수 있는 언어는 일상생활에서 사용하는 언어와는 다른 기계어(machine language)다.

- 고급 언어로 작성된 소스는 컴퓨터가 바로 이해할 수 없기 때문에 컴파일 과정을 통해 컴퓨터가 이해할 수 있는 기계어로 변환한 후 컴퓨터가 사용하게 된다.

- C, C++, java는 모두 고급 언어에 속한다. 이 언어들로 작성된 내용을 소스라고 부르고, 이 소스는 컴파일러라는 소프트웨어에 의해 기계어로 변환된 후 컴퓨터에서 실행할 수 있게 된다.


## 📚1.2 자바란?

### 1.2.1 자바 소개

- 자바 언어를 발표한 1995 - 1999년까지는 윈도우 프로그램 개발이 주류였기 때문에 C++언어에 비해 자바는 열세였다. 하지만 1999년부터 인터넷이 활성화되면서 자바가 급부상했다. 다양한 서버 운영체제에서 단 한 번의 작성으로 모든 곳에서 실행 가능한 언어는 자바뿐이었기 때문에


### 1.2.2 자바의 특징

- 이식성이 높음

- 객체 지향 언어이다 : 자바는 아무리 작은 프로그램이라도 객체를 만들어 사용한다. 캡슐화, 상속, 다형성 기능을 완벽하게 지원하고 있다.

- 함수적 스타일 코딩을 지원한다 : 자바는 함수적 프로그래밍을 위해 람다식을 자바8부터 지원한다. 람다식을 사용하면 컬렉션의 요소를 필터링, 매핑, 집계 처리하는데 쉬워지고, 코드가 매우 간결해진다.

- 메모리를 자동으로 관리한다 : C++은 메모리에 생성된 객체를 제거하기 위해 개발자가 직접 코드를 작성해야 하지만, 자바는 자동적으로 사용하지 않는 객체를 제거시켜준다.

- 막강한 오픈소스 라이브러리가 풍부하다 : 검증된 오픈소스 라이브러리를 사용하면 개발 기간을 단축하면서 안전성이 높은 애플리케이션을 쉽게 개발할 수 있다. 많은 회사들이 자바를 선택하는 이유 중 하나다.


- 장점 : write once, run anywhere(한 번 작성하면 어디서든 실행된다)

- 단점 : 느리다. 그러나 기계어로 빠르게 변환해주는 JVM, JIT 컴파일러를 통해 속도의 격자는 많이 줄고있다.


## 📚1.3 자바 개발 환경 구축

### 1.3.1 API 도큐먼트

- 자바 프로그램을 개발하기 위해서는 JDK에서 제공하는 표준 클래스 라이브러리를 반드시 사용해야 한다. 이 클래스는 API라고도 하는데, 매우 방대하기 때문에 쉽게 찾을 수 있도록 API 도큐먼트를 제공한다.

- http://docs.oracle.com/javaase/8/docs/api/

- 이클립스에서는 .찍으면 나온다.


```js
package chapter01;
public class Hello {

//자동완성 단축키 : Ctrl + Space
//우분투 : Alt + /
//Ctrl + Space : 한영전환
//windows -> preferences -> keys

public static void main(String[] args) {
System.out.println("java 첫날 설치 고생하셨습니다.");
    }
}
```


```js
package day2;
public class stringTest {
public static void main(String[] args) {

// 변수 선언 : 타입 변수명 = 초기값;

String a = "Hello world";

System.out.println(a); //Hello world
System.out.println(a.contains("ll")); //true(ll이 포함되었는지 확인)
System.out.println(a.endsWith("World")); //false(endsWith : ~로 끝났니?)
System.out.println(a.endsWith("Milkis")); //false
System.out.println(a.length()); //11
}
}
```


## 📚1.4 자바 프로그램 개발 순서

### 1.4.1 소스작성에서부터 실행까지

- 순서 : .java 소스 파일 작성 → 컴파일러로 클래스 생성 → JVM 구동 명령어로 실행

- 자바 프로그램을 개발하기 위해서는 우선 파일 확장명이 .java인 텍스트 파일을 생성하고 프로그램 소스를 작성한다. 이렇게 만들어진 파일을 자바 소스 파일이라고 한다. 작성 완료된 자바 소스 파일은 컴파일러로 컴파일해야 한다. 컴파일이 성공되면 확장명이 .class인 바이트 코드 파일이 생성된다.


### 1.4.2 소스 파일 작성 시 주의 사항


```js

package day2;


public class Hello {

public static void main(String[] args) {

System.out.println("Hello, welcome to the java world");

}


}

```

- 1라인에서 Hello의 H가 대문자로 작성되어야 한다.(파일명과 대소문자가 동일해야 한다.)

- 2라인에서 String의 S가 대문자로 작성되어야 한다.

- 3라인 끝에 세미콜론(;)을 붙여준다.


### 1.4.3 프로그램 소스 분석

- 자바 실행 프로그램은 반드시 클래스(class)블록과 main() 메소드(method) 블록으로 구성되어야 한다. 메소드 블록은 단독으로 작성될 수 없고 항상 클래스 블록 내부에서 작성되어야 한다.

- 클래스 : 필드 또는 메소드를 포함하는 블록(이름은 개발자 마음대로 정할 수 있지만, 소스파일명과 대소문자가 일치해야 한다.숫자로 시작할 수 없고, 공백을 포함해서도 안 된다.)

- 메소드 : 어떤 일을 처리하는 실행문들을 모아 놓은 블록


## 📚1.5 주석과 실행문

### 1.5.1 주석 사용하기

- 주석은 프로그램 실행과는 상관없이 코드에 설명을 붙인 것을 말한다.

- 설명이 필요한 코드에 주석을 달아 두는 것이 좋다. 복잡한 코드일수록 주석을 달면 코드를 이해하기 쉽고, 수정이 용이하다. 본인이 작성한 코드를 다른 사람이 볼 필요가 있다면 넣어주는 것이 좋다.

- // : 행 주석

- /* ~ */ : 범위 주석


### 1.5.2 실행문과 세미콜론

- 실행문을 작성할 때 주의할 점은 실행문의 마지막에 반드시 세미콜론을 붙여서 실행문이 끝났음을 표시해주어야한다.


## 📚1.6 이클립스


### 1.6.1 프로젝트 생성


- 이클립스에서 자바 소스 파일을 작성하려면 우선 자바 프로젝트를 생성해야 한다. [File → New → Java project]를 차례대로 클릭하면 new java project 대화상자가 나타나는데, project name 입력란에 프로젝트명을 입력하면 된다.


### 1.6.2 소스 파일 생성과 컴파일

- Package Explorer 뷰에서 프로젝트의 src 폴더를 선택하고 [마우스 오른쪽 버튼 → New → Class]를 선택하면 [New Java Class] 대화상자가 나온다.



## 📚2.1 변수


### 2.1.1 변수란?

- 프로그램은 작업을 처리하는 과정에서 필요에 따라 데이터를 메모리에 저장한다. 이때 변수를 사용하는데, 변수는 값을 저장할 수 있는 메모리의 공간을 의미한다. 변수란 이름을 갖게 된 이유는 수시로 값이 변동될 수 있기 때문이다. 하나의 값만 저장할 수 있다.


### 2.1.2 변수의 선언

- 변수를 사용하기 위해서는 먼저 변수를 선언해야 한다. 어떤 타입의 데이터를 저장할 것인지 그리고 변수 이름이 무엇인지를 결정한다.

```
int(타입) age(변수이름) : int(정수)값을 저장할 수 있는 age 변수 선언
double(타입) value(변수이름) : double(실수)값을 저장할 수 있는 value 변수 선언
```

- 변수의 첫 번째 글자는 숫자로 시작할 수 없다.

- 영어 대소문자가 구분된다. firstname과 firstName은 다른 변수


### 2.1.3 변수의 사용

- 변수값 저장

```js
int score; // 변수 선언
score = 90; // 값 저장
```

- 초기값은 변수를 선언함과 동시에 줄 수도 있다.

```js
int score = 90;
```


- 변수값 읽기 : 변수는 초기화가 되어야 읽을 수가 있고, 초기화되지 않은 변수는 읽을 수가 없다.

- 잘못된 예 : 변수 value가 선언되었지만, 초기화가 되지 않았기 때문에 산술 연산식 value + 10에서 사용할 수 없다.

```js
int value; //변수 value 선언(초기화 안 됨)
int result = value + 10; //변수 value 값을 읽고 10을 더한 결과값을 변수 result에 저장
```
- 잘못된 예의 수정
```js
int value = 30; //변수 value가 30으로 초기화
int result = value + 10; //변수 value 값을 읽고 10을 더한 결과값(40)을 변수 result에 저장
```


### 2.1.4 수의 사용 범위

- 변수는 중괄호{} 블록 내에서 선언되고 사용된다. 메소드 블록 내에서 선언된 변수를 로컬 변수라고 부른다. 로컬 변수는 메소드 실행이 끝나면 메모리에서 자동으로 없어진다.

- 변수는 선언된 블록 내에서만 사용이 가능하다.

- 메소드 블록 내에서도 여러 가지 중괄호 {}블록들이 있을 수 있다. 조건문에 해당하는 if, 반복문에 해당하는 for, while 등이 중괄호를 가질 수 있다. If, for, while을 제어문이라고 하는데, 제어문 블록에서 선언된 변수는 해당 제어문 블록 내에서만 사용이 가능하고 블록 밖에서는 사용할 수 없다.

- 따라서 변수를 선언할 때에는 변수가 어떤 범위에서 사용될 것인지를 생각하고, 선언 위치를 결정해야 한다.

- 메소드 블록에서 어떤 위치에서건 사용할 수 있도록 한다면 메소드 블록 첫 머리에 선언하는 것이 좋다.

- 제어문 내에서 잠깐 사용되는 변수라면 제어문 내에서 선언하는 것이 좋다.


```js
package day2;
public class oper {
public static void main(String[] args) {

int a = 5;               //항상 변수를 초기화 먼저 하고 연산
int b = a + 10 - 6 ;     // = 할당(대입) 연산자 : 오른쪽의 결과(a+10-6)를 왼쪽에 전달(b)
System.out.println(b);   // 9

a = b + a + 2 ;
System.out.println(a); //16

int i = 10;
int j = 4;

//사칙연산 : +, -, *, /

System.out.println(i+j); //14
System.out.println(i+j*3-10); //12
// 기본적으로 왼쪽에서 오른쪽으로 계산, 연산자 우선순위가 있어 우선순위를 먼저 처리합니다.
}
}
```

## 📚2.2 데이터 타입
### 2.2.1 기본 타입
- 정수 : byte, char, short, int, long(실제론 거의 int와 long만 사 )
- 실수 : float, double
- 논리 : boolean

### 2.2.2 정수 타입(byte, char, short, int, long)
-  byte의 경우 -128(최소값)부터 시작해서 127(최대값)을 넘으면다시 -128부터 시작하게 된다. 다른 정수 타입인 short, int, long 역시 마찬가지다.
```js
package day3;

public class Garbage {
	public static void main(String[] args) {
		byte var1 = 125;
		int var2 = 125;
		
		for(int i = 0; i<5; i++) {
			var1++;	//i = i = 1
			var2++;
			System.out.println("var1 : " + var1 + "\t" + "var2: " + var2);
		}
	}
}
/*
var1 : 126	var2: 126
var1 : 127	var2: 127
var1 : -128	var2: 128
var1 : -127	var2: 129
var1 : -126	var2: 130

이와 같이 저장할 수 있는 값의 범위를 초과해서 값이 저장될 경우 엉터리 값이 변수에 저장되는데, 이걸 쓰레기 값이라고 한다. 개발자는 쓰레기값이 생기지 않도록 주의해야 한다.
Byte 변수는 127을 넘어서는 순간 최소값인 -128부터 다시 저장되는 것을 볼 수있고, int타입의 변수는 정상적으로 1 증가된 값을 계속 저장하는 것을 볼 수 있다.
*/

- char 타입 : 자바는 모든 문자를 유니코드로 처리한다. 유니코드는 세계 각국의 문자들을 코드값으로 매핑한 국제 표준 규약이다. 유니코드는 하나의 문자에 대해 하나의 코드값을 부여하기 때문에 영문 ‘A’ 및 한글 ‘가’도 하나의 코드값을 가진다. http://www.unicode.org 에서 찾을 수 있다.
- char 타입 변수에 작은 따옴표로 감싼 문자를 대입하면 해당 문자의 유니코드가 저장된다.

```js
package day3;

public class sasw {
	public static void main(String[] args) {
		char c1 = 'A' ;					//A : 문자를 직접 저장
		char c2 = 65;						//A : 10진수로 저장
		char c3 = '\u0041';				//A : 16진수로 저장
		
		char c4 = '가';					//가 : 문자를 직접 저장
		char c5 = 44032;					//가 : 10진수로 저장
		char c6 = '\uac00';				//가 : 16진수로 저장
		
		int uniCode = c1;					//65 : 유니코드 얻기

		System.out.println(c1);
		System.out.println(c2);
		System.out.println(c3);
		System.out.println(c4);
		System.out.println(c5);
		System.out.println(c6);
		System.out.println(uniCode);
	}
}
```

- System.out.println(); 은 변수의 타입이 char이면 유니코드에 해당하는 문자를 출력하는 것을 볼 수 있다. Char 타입 변수는 단 하나의 문자만 저장한다. 만약 문자열을 저장하고 싶다면 String 타입을 사용해야 하는데  String 변수를 선언하고 큰 따옴표로 감싼 문자열 리터럴을 대입하면 된다.
```js
package day3;

public class testwon {
	public static void main(String[] args) {
		String c1 = "홍길동" ;	//String 변수 선
		System.out.println(c1);	// 홍길동
	}
}
```
```js
package day3;
public class testwon {
	public static void main(String[] args) {
		String c1 = "홍길동";					
		System.out.println("나는" + c1);	//나는홍길동  
	}
}

- A~Z까지 해보기
```
```js
package day3;

public class asd {
	public static void main(String[] args) {
		char c1 = 'A';
		for(int i = 0; i<26; i++) {	//for 에는 i
			System.out.println(c1);		
		c1++;							//A~Z 흐름 보고 뭐가 어디에 들어가는지 보
		}
	}
}
```

- int타입 : 자바에서 정수 연산을 하기 위한 기본 타입이다. Byte 와 short의 변수를 연산하면 int 타입으로 변환되고 결과 역시 int 타입이 된다.


```js
package day4;				//변환으로 인한 데이터 손실이 발생되지 않도록 한다.
public class sswon {

	public static void main(String[] args) {
		int i = 128;
		
		if((i<Byte.MIN_VALUE) || (i>Byte.MAX_VALUE)) {					//(i<-128)||(i>127)과 동일
			System.out.println("byte 타입으로 변환할 수 없습니다.");
			System.out.println("값을 다시 확인해 주세요");

		}else{
		byte b = (byte) i ;
		System.out.println(b);
		}
 
	}

}

```
```js
package day4;

public class sswontest {

	public static void main(String[] args) {
			int i = 25;
			
			if((i<Byte.MIN_VALUE) || (i>Byte.MAX_VALUE)) {					//(i<-128)||(i>127)과 동일
				System.out.println("byte 타입으로 변환할 수 없습니다.");
				System.out.println("값을 다시 확인해 주세요");

			}else{
			byte b = (byte) i ;
			System.out.println(b);			// i가 -128 ~ 127 사이이므로 값이 나옴
			}
	
		}
	}
```

- 정수 타입을 실수 타입으로 변환할 때 정밀도 손실을 피한다.
Int 값을 손실 없이 float 타입 값으로 변환할 수 있으려면 가수 23비트로 표현 가능한 값이어야 한다. 123456780은 23비트로 표현할 수 없기 때문에 근사치로 변환된다. 즉 정밀도 손실이 발생한다. 그렇기 
때문에 float 값을 다시 int 타입으로 변환하면 원래의 int 값을 얻지 못한다.

### 2.3.3 연산식에서의 자동 타입 변환
- 연산은 기본적으로 같은 타입의 피연산자 간에만 수행되기 때문에 서로 다른 타입의 피연산자가 있을 경우 두 피연산자 중 크기가 큰 타입으로 자동 변환된 후 연산을 수행한다.
```js
package day4;

public class FromIntToFloat {

	public static void main(String[] args) {
		String a = "A";
		char a2 = (char)a;  // String은 char 캐스팅 안 된다. String은 특이
		
	}

}
```


### 2.2.3 실수 타입(float, double)

- long
```js
package day3;

public class Vari {

	public static void main(String[] args) {
		byte a = 3;
		byte b = 5;
		//byte c = a + b; // 산술연산시 내부적으로 int 결과가 나옴
		byte c = (byte)(a+b); 				// casting
		System.out.println("c=" + c);		// c=8
		long d = 100000000000L; 				// 수치가 큰 데이터가 들어가 l값이 들어가야 됨
		float f1 = 0.1F;
		float f2 = 0.2F;
		float f3 = f1 + f2;
		System.out.println("f3=" + f3);
	}

}
```

### 2.2.4 논리타입(boolean)

- boolean은 true/false를 저장할 수 있는 데이터 타입이다. 두 가지 상태값을 저장할 필요성이 있을 때 사용됨

## 📚2.3 타입변환
### 2.3.1 자동 타입 변환
- 자동 타입 변환은 프로그램 실행 도중에 자동적으로 타입 변환이 일어나는 것을 말한다. 작은 크기를 가지는 타입이 큰 크기를 가지는 타입에 저장될 때 발생한다.
```
- byte1 → short2 → int4 → long8 → float4 → double8
```

### 2.3.2 강제 타입 변환
- 큰 크기의 타입은 작은 크기의 타입으로 자동 타입 변환을 할 수 없다. 강제적으로 큰 데이터 타입을 작은 데이터 타입으로 쪼개어서 저장하는 것을 강제 타입 변환이라고 한다. 강제 타입 변환은 캐스팅 연산자 ()를 사용하는데, 괄호 안에 들어가는 타입은 쪼개는 단위이다.

## 📚3.1 연산자와 연산식

- 산술 : + - * % / 		숫자			사칙연산, 나머지 계산
- 부호 : + -			숫자			음수와 양수의 부호
- 문자열 : +			문자열			두 문자열을 연결
- 대입 := += -= *= /=…	다양 			우변의 값을 좌변의 변수에 대입
- 증감 : ++ – 		숫자			1만큼 증감
- 비교 : == != < > >= <= 	boolean		값의 비교
- 논리 : ! & | && || 	boolean		논리적 not and or
- 조건 : (조건식)?A:B	숫자, boolean	조건식에 따라 A또는B 중 하나를 선택
- 비트 : ~ & | ^ 		숫자, boolean 	비트 not and or xor연산
- 쉬프트 : >> << >>> 	숫자 			비트를 좌우로 밀어서 이동


```js
package day4;

public class Oper {
	public static void main(String[] args) {
		/* 	우선순위
		 * 	1. ()
		 * 	2. *, /,&
		 * 	3. + , -
		 *  4. !
		 *  5. &&
		 *  6. ||
		 */
		int a = 10;
		// a에 1을 더해라
		//a++;
		//a = a + 1 ;
		a += 1; // a = a + 1 간략하게 바꾼 것, -도 마찬가지로 생각하면  
		System.out.println(a);
		
	}

}
```




### 3.1.1 증감 연산자
- ++피연산자 : 다른 연산자를 수행하기 전! 피연산자의 값을 1 증가시킴
- 피연산자++ : 다른 연산을 수행한 후! 피연산자의 값을 1 증가시킴
```js
package day3;
public class Vari {

	public static void main(String[] args) {
		int a = 10;
		int b = a++;
		System.out.println("b=" + b);		//b=10
		
		int c = ++b;
		System.out.println("c=" + c);		//c=11
```
```js
Package day3;

public class Vari {

	public static void main(String[] args) {
		int a = 10;
		int b = a++ + a++ + a++ ; 		//10+11+12 = 33
		System.out.println("b=" + b);
```
### 3.1.2비트 연산자(&&, ||, &, |, ^, !)
- AND : 두 비트 모두 1일 경우에만 1
- OR : 두 비트 중 하나만 1이면 1
- XOR : 두 비트 중 하나는 1이고 다른 하나가 0일 경우 1
- NOT :  보수(반대의 값,1이면 0, 0이면 1)
 

### 3.1.2 논리 부정 연산자(!)
- 논리 부정 연산자는 true를 false로, false를 true로 변경하기 때문에 boolean 타입에만 사용가능하다.

### 3.1.3 비트 반전 연산자(~)
- 비트 반전 연산자는 정수 타입의 피연산자에만 사용되며, 피연산자를 2진수로 표현했을 때 비트값인 0을 1로, 1은 0으로 반전한다. 연산 후, 모든 비트가 반전되기 때문에, 부호가 반대인 새로운 값이 산출된다.

```js
package day4;

public class Oper {
	public static void main(String[] args) {

		int v1 = 10;
		int v2 = ~v1 + 1;
		int v3 = -v1;
		
		System.out.println(("v2=" + v2 ));
		System.out.println("v3=" + v3);
		System.out.println("v1=" + Integer. toBinaryString(v1));
		System.out.println("v2=" + Integer. toBinaryString(v2));
	}

}
```

### 3.2.1  산술 연산자
- + : 덧셈
- - : 뺄셈
- * : 곱셈
- / : 나눗셈
- % : 좌측을 우측으로 나눈 나머지를 구하는 연산

```js
package day4;

public class FromIntToFloat {

	public static void main(String[] args) {
		int size = 1048000 ;
		if(size < 1024) {	
			System.out.printf("%d byte %n",size);
		}else if(size <(1024 * 1024)) {
			System.out.printf("%.2f Kb %n", size / 1024.0);
		}else {
			System.out.printf("%,2f Mb %n",size / (1024* 1024.0));		//10203.44Kb
		}
		
		String name = "홍길동";
		int age = 26 ;
		String address = "대전 중구 ..";
		System.out.printf("%5s님 은 %3d살 사는 곳은 %-20s %n", name, age, address);
int x1= 5;
int x2 = x1 / 0;			//에러가 나면 예외처리를 해야된다. 10장에서 배움...
		System.out.println("어제 새벽에 바람 많이불음..");

		try {
			int x1= 5;
			int x2 = x1 / 0;				//컴파일에서는 오류X, 실행시 오류 발
			
		} catch (Exception e) {	
			// 예외가 나면 catch가 잡아서 밑에 걸 실행, 예외 안 나면 그대로 쭉
			System.out.println("예외가 발생했어요.."+e.getMessage());
			e.printStackTrace();
	}	
	}

```

### 3.2.2 문자열 연결 연산자(+)
+ 연산자는 산술 연산자, 부호 연산자인 동시에 문자열 연결 연산자이기도 하다. 피연산자 중 한쪽이 문자열이면 +연산자는 문자열 연결 연산자로 사용되어 다른 피연산자를 문자열로 변환하고 서로 결합한다.
```js
String str1 = “JDK” + 6.0; // JDK6.0
```
```js
		System.out.println(3*4+"십이");		//12십이
		System.out.println("Hi" + (3 * 4));		//Hi12
```

### 3.2.3 비교연산자

```js
String strVar1 = “사승원”;
String strVar2 = “사승원”;
String strVar3 = new String(“사승원”);

```
- 자바는 문자열 리터럴이 동일하다면 동일한 String 객체를 참조하도록 되어있다. 그래서 변수 strVar1과 strVar2는 동일한 String 객체의 번지값을 가지고 있다. 그러나 변수 strVar3은 객체 생성 연산자인 new로 생성한 새로운 string 객체의 번지값을 가지고 있다.

```js
strVar1 == strVar2 // true
strVar2 == strVar3 // false
```

- 이경우 변수 strVar1과 strVar2의 == 연산은 true를 산출하고 strVar2와 strVar3의 == 연산은 false를 산출한다.

- String 객체의 문자열만 비교하고 싶다면 == 연산자 대신 equals()메소드를 사용해야 한다. equals()메소드는 문자열이 동일한지 비교한 후 true 또는 false를 리턴한다.

```js
strVar1.equals(strVar2) //true
strVar2.equals(strVar3) //true
```

### 3.2.4 논리연산자
- &&는 앞의 피연산자가 false라면 뒤의 피연산자를 평가하지 않고 바로 false라는 결과를 낸다. 하나라도 false라면 전체 연산식은 flase이기 때문이다. 그러나 &는 두 피연산자 모두를 평가해서 산출 결과를 낸다. 따라서 &보다 &&가 더 효율적으로 동작한다. || 와 |도 같은 형식으로 동작한다. 따라서 || 가 더 효율적으로 작동한다. 논리연산은 흐름제어문인 조건문(if), 반복문(for, while) 등에서 주로 이용된다.

- 비트 이동 연산(<<, >>, >>>) 비트 이동 (shift) 연산자는 정수 데이터의 비트를 죄측 또는 우측으로 밀어서 이동시키는 연산을 수 행한다

- a << b : 정수a 의 각 비트를 b만큼 왼쪽으로 이동(빈자리는 0 으로 채워진다.) a << b : 정수 a 의 각 비트를 b 만큼 오른쪽으로(빈자리는 정수 a의 최상위 부호 비트 (MSB)와 같은 값으로 채워진다.) a >>>b : 정수 a 의 각 비트를 b만큼 오른쪽으로 이동(빈자리는0 으로 채워진다.)

```js 
package day5;

public class dddddddd {

	public static void main(String[] args) {
		System.out.println('A'==65);			//true
		System.out.println(3==3.0);				//true
		System.out.println(0.1==0.1f);			//false
		System.out.println("------------------");
	
		//문자열인 경우 비교
		String strA = "홍길동";
		String strB = "홍길동";
		String strC = new String("홍길동");
		System.out.println("strA == strB" + (strA == strB)); //strA == strBtrue
		System.out.println("strA == strC" + (strA == strC)); //strA == strCfalse	
		// 문자열은 비교연산자를 사용 못함(>,< >=, <=)
		// System.out.println("strA > strC =" + (strA > strC))
		
		strA = "A";
		strB = "a";
		char chrA = 'c';
		char chrB = 'a';
		System.out.println("chrA > chrB=" +(chrA > chrB));		//chrA > chrB=true
		System.out.println(strA.compareTo(strB));					//-32
		System.out.println(strA.compareToIgnoreCase(strB));		//0
		
		System.out.println("------------------");
		
		int intA = 678;
		System.out.println("(intA >> 1)=" + (intA >> 1));		//(intA >> 1)=339
		System.out.println("(intA >> 2)=" + (intA >> 2));		//(intA >> 2)=169
		System.out.println("(intA >> 3)=" + (intA >> 3));		//(intA >> 3)=84

		System.out.println("(intA << 1)=" + (intA << 1));		//(intA << 1)=1356
		System.out.println("(intA << 2)=" + (intA << 2));		//(intA << 2)=2712
		System.out.println("(intA << 3)=" + (intA << 3));		//(intA << 3)=5424
		
		System.out.println("-------운동취미---------");
		
			//4 : 축구, 3 : 야구, 2 : 농구, 1 : 배구
			//0000 1111 : 15
			//0000 1000 : 8
			//0000 0100 : 4
			//0000 0010 : 2
			//0000 0001	: 1 
		 int hobby = 15;
		// 출력을 "취미는 축구, 야구, 농구, 배구 입니다."
		String result = "";
		if (((hobby >> 3) & 1) == 1) {
			//result = result + "축구";
			result += "축구";  // 짧게 이렇게 표현할 수도 있다.
		}
		if (((hobby >> 2) & 1) == 1) {
			result = result + "야구";
		}
		if (((hobby >> 1) & 1) == 1) {
			result = result + "농구";
		}
		if ((hobby & 1) == 1) {
			result = result + "배구";
		
		result = "취미는" + result + "입니다.";
		System.out.println(result);
			
		}
	}
}

		System.out.println("---------삼항연산자---------");
	
		int score = 95;
		String grade = "";
		if(score > 90) {	//if문 뒤에 ; 붙이면 끝난 것으로 보기 때문에 else 뒤에 ;하기 
			grade = "참 잘했어요!!";
			} else { 
			grade = "그래도 잘했어!!";
		}
				System.out.println(grade);
		
		System.out.println("---------삼항연산자 문제---------");
		
		// 위 score에 따라서 grade를 삼항연산자로 해주세요 
		
		int score = 55;
		String grade = (score > 90) ? "참 잘했어요!!" : "그래도 잘했어!!";
		System.out.println(grade);			// 그래도 잘했어!! 
	}
		// 삼항연산자로 더 간결하게 표현 가능

```

# 04 조건문과 반복문

## 📚4.1 데이터 타입

### 4.1.1 if문

```js
package day5;
public class If {

	public static void main(String[] args) {
		int score = 99 ;
		String grade = "";
		
		if(score >= 90) {
			grade = "참 잘했어요";
		}
		if(score >= 80) {
			grade = "잘했어요";
		}
		if(score >= 70) {
			grade = "했어요";
		}
		if(score < 70) {
			grade = "뭐해..?";
		}
		System.out.println(grade);	//했어요
			
		// 참 잘했어요가 나와야 하는데  했어요가 실행됨..
		// 이런 것 때문에 if-else 가 필요.
	}
}
```

### 4.1.2 else if문
```js
package day5;

public class If {
	public static void main(String[] args) {
		int score = 97 ;
		String grade = "";
		
		if(score >= 90) {
			grade = "참 잘했어요";	//그냥 if문과 달리 else if 문은
							//위에가 참이면 밑에는 실행되지 않음.
			grade = "참 잘했어요";		//그냥 if문과 달리 else if 문은 위에가 참이면 밑에는 실행되지 않음.

		}else if(score >= 80) {
			grade = "잘했어요";
		}else if(score >= 70) {
			grade = "했어요";
		}else {
			grade = "뭐해..?";
		}
		System.out.println(grade);		//참 잘했어요
	}
}
```

### 4.1.3 Math.random

```js
package day6;

public class IfDiceExample {

	public static void main(String[] args) {
		
		int num = (int)(Math.random()*6) + 1;	
		//int(정수값을 얻기 위해), Math.random()*6(마지막 숫자는 6), +1(시작 숫자)
		
		if(num == 1) {
			System.out.println("1번이 나왔습니다.");
		}	else if(num == 2) {
			System.out.println("2번이 나왔습니다.");
		}	else if(num == 3) {
			System.out.println("3번이 나왔습니다.");
		}	else if(num == 4) {
			System.out.println("4번이 나왔습니다.");
		}	else if(num == 5) {
			System.out.println("5번이 나왔습니다.");
		}	else	{
			System.out.println("6번이 나왔습니다.");
		}
	}

}
```
- 오늘의 문제
```js
package day6;
public class elseif02 {

	public static void main(String[] args) {
		//국어,영어,수학 값을 랜덤하게 생성해서
		//점수는 1~100사이, 평균은 구한 합의 /3
		//평균, 합계를 구해주세요
		
		double avg = 0;

		int kor = (int)(Math.random()*100) +1;
		int eng = (int)(Math.random()*100) +1;
		int mat = (int)(Math.random()*100) +1;

		int sum = (int)(kor + eng + mat) ;
		int sum = (int)(kor + eng + mat) ; 
		avg = (double)(kor + eng + mat / 3);
		
		System.out.println("국어\t영어\t수학\t총점\t평균");
		System.out.printf("%d\t%d\t%d\t%d\t%f\n"
								,kor, eng, mat, sum, avg);
	}
}
//int kor = 0, eng = 0, mat = 0, sum = 0;
//double avg = 23.34556454;
```
- 변형문제
```js
package day6;
public class elseif02 {

	public static void main(String[] args) {
		//국어,영어,수학 값을 랜덤하게 생성해서
		//점수는 1~100사이, 평균은 구한 합의 /3
		//평균, 합계를 구해주세요
		//평균 점수가 90이상이면 "A", 80이상이면 "B",
		//70이상이면 "C", 60이상이면 "D" 그외는 "F" 출력
		
		double avg = 0;
		String grade = "";	//F를 주고 else를 안 쓰는 방법도 있음

		int kor = (int)(Math.random()*100) +1;
		int eng = (int)(Math.random()*100) +1;
		int mat = (int)(Math.random()*100) +1;
		int sum = (int)(kor + eng + mat) ;
		avg = (double)((kor + eng + mat) / 3);
		//avg = sum / 3.0 ; -> 이렇게도 가능(정수 나누기 정수는 정수. 소수점 이하는 버림)
		
		if(avg >= 90) {
			grade = "A";
		} else if(avg >= 80) {
			grade = "B" ;
		} else if(avg >= 70) {
			grade = "C" ;
		} else if(avg >= 60) {
			grade = "D" ;
		} else {
			grade = "F" ;
		}
		
		System.out.println("국어\t영어\t수학\t총점\t평균\t등급");
		System.out.printf("%d\t%d\t%d\t%d\t%.2f\t%s\n"
								,kor, eng, mat, sum, avg, grade);
	}
}
```

### 4.1.4 Scanner
```js
package day7;
import java.util.Scanner ; //이걸 갖다 놓고 사용해야함
public class IfIf {
	
	public static void main(String[] args) {
		//이름, 국어, 영어, 수학 점수를 콘솔에서 입력받아서
		//국어,영어,수학 값을 랜덤하게 생성해서
		//점수는 1~100사이, 평균은 구한 합의 /3
		//평균, 합계를 구해주세요
		//평균 점수가 90이상이면 "A", 80이상이면 "B",
		//70이상이면 "C", 60이상이면 "D" 그외는 "F" 출력
		
		double avg = 0;
		String name = "";	
		Scanner scanner = new Scanner(System.in);
		System.out.println("이름, 국어, 영어, 수학 점수를 순서대로 입력해주세요");
		
		name = scanner.next() ;  
		int kor = scanner.nextInt() ;
		int eng = scanner.nextInt() ;
		int mat = scanner.nextInt() ;
		int sum =(kor + eng + mat) ;
		avg = 56 / 3.0 ;
		//avg = sum / 3.0 ; -> 이렇게도 가능(정수 나누기 정수는 정수. 소수점 이하는 버림)
		String grade ;
		if(avg >= 90) {
			grade = "A";
		} else if(avg >= 80) {
			grade = "B" ;
		} else if(avg >= 70) {
			grade = "C" ;
		} else if(avg >= 60) {
			grade = "D" ;
		} else {
			grade = "F" ;
		}
		
		System.out.println("이름\t국어\t영어\t수학\t총점\t평균\t등급");
		System.out.printf("%s\t%d\t%d\t%d\t%d\t%d\t%.2f\t%s\n"
								, name, kor, eng, mat, sum, avg, grade);
		
	}
```
```js

	public static void mainScan(String[] args) {
		// p.126 사용자 입력
		//System.in.read() 바이트 단위 입력(0~255, 스트림의 끝이면 -1)
		//System.in.read()
		Scanner scanner = new Scanner(System.in);
		//next() : 공백이전까지의 문자열 리턴
		//next + 타입() : nextInt(), nextDouble()
		//nextLine() : 문자열 전체 리턴
		//홍길동 25 True
		System.out.println("이름과 나이 결혼여부(true/false)");
		String name = scanner.next();
		int age = scanner.nextInt();
		boolean marriage = scanner.hasNextBoolean() ;
		System.out.println( name + "님" + age + "살, 결혼은" + marriage);
		
		scanner.close() ;
	}
}
```


### 4.1.5 switch문

```js
package day7;

public class Switch01 {

	public static void main(String[] args) {
		int num = (int)(Math.random() *6) + 1 ;
		System.out.println("구한 num=" + num);
		// switch(표현식) : 표현식은 기본적으로 정수형 + JDK 1.7부터 문자열 가능
		switch (num) { //(num -1) 같은 연산이 올 수도 있음
		case 1 : System.out.println("1이 나왔어요"); break ;
		case 2 : System.out.println("2이 나왔어요");break ;
		case 3 : System.out.println("3이 나왔어요");break ;
		case 4 : System.out.println("4이 나왔어요");break ;
		case 5 : System.out.println("5이 나왔어요");break ;
		default : System.out.println("6이 나왔어요");break ;
		}
	}
}
```
```js
package day7;
import java.util.Scanner;
public class ex {

	public static void main(String[] args) {
		Scanner scan = new Scanner(System.in);
		System.out.println("원하시는 월을 입력하세요[1~12]");
		int month = scan.nextInt();
		int maxday = 0; 	// =0에 의미를 두지말
		
//		switch (month) {
//		case 1 : maxday = 31; break ;
//		case 2 : maxday = 28; break ;
//		case 3 : maxday = 31; break ;
//		case 4 : maxday = 30; break ;
//		case 5 : maxday = 31; break ;
//		case 6 : maxday = 30; break ;
//		case 7 : maxday = 31; break ;
//		case 8 : maxday = 31; break ;
//		case 9 : maxday = 30; break ;
//		case 10 : maxday = 31; break ;
//		case 11 : maxday = 30; break ;
//		default : maxday = 31; break ;
		
		switch (month) {
		case 1 :
		case 3 :
		case 5 :
		case 7 :
		case 8 :
		case 10 :
		case 12 : maxday = 31; break ;
		case 2 : maxday = 28; break ;
		case 4 :
		case 6 :
		case 9 :
		case 11 : maxday = 30; break ;
		default : System.out.println("월이 정확하지 않습니다.");break ;
	}
		System.out.println(month + "월은" + maxday + "일까지 존재합니다.");	
		//syso 마지막에 출력하려면 괄호를 나와서 마지막에
	}
}
```

## 📚 4.2 반복문(for문, while문, do~while문)

### 4.2.1 for
- 기본적인 구조
```js
int sum = 0;
for (int i = 1; i <=100; i++ ) {
	sum = sum +1 ;
}
System.out.println("1~100까지의 합:"+sum);
```
>for ((1)초기회식; (2)조건식; (4)증감식)
>		     (3)실행문 – true일 때
>false일 경우 for문 종료

- 1부터 100까지의 홀수의 합을 구해라(오답)
```js
package day7;

public class Question {

	public static void main(String[] args) {
	 //1부터 100까지의 홀수의 합 얼마인가요?
		int sum = 0 ;
		for(int i = 1 ; i < 100 ; i++) {
			sum =  sum + (i+2);
		}
		System.out.println("1부터 100까지의 홀수의 합 =" +sum);
	}
}
```
- 1부터 100까지의 홀수의 합을 구해라(정답)
```js
package day7;

public class Question {

	public static void main(String[] args) {
	 //1부터 100까지의 홀수의 합 얼마인가요?
		int sum = 0 ;
		for(int i = 1 ; i < 100 ; i++) { //i = i + 2
			if(i % 2 ==1)
			sum =  sum + i; // sum += i;
		}
		System.out.println("1부터 100까지의 홀수의 합 =" +sum);
	}
}
```

- 1부터 100까지의 3의 배수의 합(오답)
```js
package day7;
public class Q2 {

	public static void main(String[] args) {
		int sum =0 ;
		for(int i = 0; i <(100/3)  ; i++) {
		   sum = sum + (i*3);
			
			System.out.println("1부터 100까지의 3의 배수의 합=" + sum);
	}
}}
```
- 1부터 100까지의 3의 배수의 합(정답)
```js
package day7;

public class Q2 {

	public static void main(String[] args) {
		int sum =0 ;
		for(int i = 1; i <= (100/3)  ; i++) {
		   sum = sum + (i*3);
	}
		System.out.println("1부터 100까지의 3의 배수의 합=" + sum);
}}

```

- 6단을 출력
```js
package day8;

public class For3 {

	public static void main(String[] args) {
		//6단을 출력
		//문자열 "i"와 숫자변수 i는 전혀 다른 것이다.
		for(int i = 1 ; i < 10 ; i++) {
			System.out.println("6 * " + i + " = " + (6 * i ));
		}
	}
}
```
- 고객이 원하는 숫자를 넣으면 원하는 구구단 나오게 하기
```js
package day8;

public class For3 {

	public static void main(String[] args) {
		//문자열 "i"와 숫자변수 i는 전혀 다른 것이다.
		//고객이 원하는 숫자 넣으면 원하는 답 나오게 하기
		danPrint(5);	// 절차형언어 : 함수, OOP:메서드
		danPrint(8);
		}
	public static void danPrint(int dan) {
		System.out.println(dan + "단");
		for(int i = 1 ; i < 10 ; i++) {
			System.out.println(dan+ " X " + i + " = " + (dan * i ));
	}
}
}
```
- 구구단
```js
package day8;

public class For05 {

	public static void main(String[] args) {
		/*
		  구구단
		 */
		for(int i = 1; i <= 9 ; i++) {
			System.out.println(i+"단");
			for(int j = 1 ; j <= 9 ; j++) {
				System.out.println(i+ "X" + j + " = " + i*j);
			}
		}
	}
}

```
- 별표출력하기
```js
package day8;

public class For03 {

	public static void main(String[] args) {
		/*
		  별 다섯개 출력하기*****
		 */
		System.out.println("*****");	
		System.out.print("*");		//ln은 엔터쳐주는 거구나
		System.out.print("*");
		System.out.print("*");
		System.out.print("*");
		System.out.print("*");
		for(int i = 0 ; i < 5 ; i++) {
			System.out.println("*");}	//ln과 차이
	    	System.out.print("*");
		System.out.println("");
		/* 1번 피라미드
 		  *
		  **
		  ***
		  ****
		  *****
		 */
		for(int i = 0 ; i < 5; i++) {
			switch(1) {
			case 0 : System.out.println("*"); break ;
			case 1 : System.out.println("**"); break ;
			case 2 : System.out.println("***"); break ;
			case 3: System.out.println("****"); break ;
			case 4 : System.out.println("*****"); break ;
			}
		}
}
}
```

- 피라미드
```js
package day8;

public class For04 {

	public static void main(String[] args) {
		/* 1번 피라미드
		1 *
		2 **
		3 ***
		4 ****
		5 *****
		 */
		for(int i = 1 ; i <= 5; i++) {
			for(int j =1 ; j <= i ; j++ ) {
				System.out.print("*");
				
			}
				System.out.println(" ");
		}
		/* 2번 피라미드
		i	j 변수의 시작값 또는 for 문의 조건식을 고민
 		1	*****
 		2	****
 		3	***
 		4	**
 		5	*
 
		*/
		for (int i = 5; i >= 1; i--) {
			for (int j = 1; j <= i; j++) {
				System.out.print("*");

			}
			System.out.println();

		}
		System.out.println("-------------------------------");
			/* 3번 피라미드
			i	j 변수의 시작값 또는 for 문의 조건식을 고민
	 		1	|     *	1=1
	 		2	|    ***	2=3
	 		3	|   *****	3=5
	 		4	|  *******	4=7
	 		5	| *********	5=9
			*/
		
		for(int i = 1 ; i <= 5; i++) {
			//별은별, 공백은 처리
			for(int k = 5; k > i ; k--) {
				System.out.print(" ");
				
			}
			for(int j = 1; j <= (i*2-1) ; j++) {
				System.out.print("*");
			}
			System.out.println();
		}
	}
}
```


### 4.2.2 while문
- for문이 정해진 횟수만큼 반복한다면, while문은 조건식이 true일 경우에 계속해서 반복한다. 조건식에는 비교 또는 논리 연산식이 주로 오는데 조건식이 false가 되면 반복 행위를 멈추고 while문을 종료한다.

```js
package day8;

import java.util.Scanner;

public class While01 {

	public static void main(String[] args) {
		// 이름, 국어, 영어, 수학 점수를 콘솔에서 입력받아서
		// 국어,영어,수학 값을 랜덤하게 생성해서
		// 점수는 1~100사이, 평균은 구한 합의 /3
		// 평균, 합계를 구해주세요
		// 평균 점수가 90이상이면 "A", 80이상이면 "B",
		// 70이상이면 "C", 60이상이면 "D" 그외는 "F" 출력
		// 홍길동 45 78 99 [엔터]
		// q 또는 Q [엔터]

		boolean run = true;
		Scanner scanner = new Scanner(System.in);
		while (run) {
			String name = "";
			double avg = 0.0;
			System.out.println("이름, 국어, 영어, 수학 점수를 순서대로 입력해주세요[종료:Q]");
			name = scanner.next();
			// name에 "Q" 또는 'q'인 경우 종료되는 조건을 설정
			// 그렇지 않다면
			if (name.equals("Q") || name.equals("q")) {
				run = false ;
			}else {
					
		
			int kor = scanner.nextInt();
			int eng = scanner.nextInt();
			int mat = scanner.nextInt();
			scanner.nextLine();
			int sum = kor + eng + mat;
			avg = sum / 3.0;
			String grade;
			if (avg >= 90) {
				grade = "A";
			} else if (avg >= 80) {
				grade = "B";
			} else if (avg >= 70) {
				grade = "C";
			} else if (avg >= 60) {
				grade = "D";
			} else {
				grade = "F";
			}

			System.out.println("이름\t국어\t영어\t수학\t총점\t평균\t등급");
			System.out.printf("%s\t%d\t%d\t%d\t%d\t%.2f\t%s\n", name, kor, eng, mat, sum, avg, grade);
			}
		}
		System.out.println("종료되었습니다.");
	}
	
//	이름, 국어, 영어, 수학 점수를 순서대로 입력해주세요[종료:Q]
//			홍길동 90 80 80
//			이름	국어	영어	수학	총점	평균	등급
//			홍길동	90	80	80	250	83.33	B
//			이름, 국어, 영어, 수학 점수를 순서대로 입력해주세요[종료:Q]
//			사승원 80 80 80
//			이름	국어	영어	수학	총점	평균	등급
//			사승원	80	80	80	240	80.00	B
//			이름, 국어, 영어, 수학 점수를 순서대로 입력해주세요[종료:Q]
//			q
//			종료되었습니다.
//	
```

### 4.2.3 do while
- do whlie 문은 조건식에 의해 반복 실행한다는 점에서는 while문과 동일하다. 
- while문은 시작할 때부터 조건식을 검사하여 블록 내부를 실행할지 결정하지만, 경우에 따라서는 블록 내분의 실행문을 우선 실행시키고 실행 결과에 따라서 반복 실행을 계속할지 결정하는 경우도 발생한다.

```js
do
{
(1) 실행문
} while (2) 조건식 : true면 실행문으로 가서 반복
false면  do whlie문 종료
```
```js
package day9;

import java.util.Scanner;										// Scanner 클래스를 사용하기 위해 필요

public class DoWhile {

	public static void main(String[] args) {
		boolean run = true;
		Scanner scanner = new Scanner(System.in);				//Scanner 객체 생성
		do {
			String name = "";
			double avg = 0.0;
			System.out.println("-----------------------------------------------");
			System.out.println("이름, 국어, 영어, 수학 점수를 순서대로 입력해주세요[종료:Q]");
			System.out.println("-----------------------------------------------");
			System.out.println("이름[종료:Q]");
			name = scanner.nextLine();							//키보드로 입력한 문자열을 얻음
			
			if(name.equals("Q") || name.equals("q"))	{		//문자열을 비교할 때는 equals("") 메소드 사
				run = false ;
			} else {
			System.out.println("국어 : ");
			int kor = Integer.parseInt(scanner.nextLine());
			System.out.println("영어 : ");
			int eng = Integer.parseInt(scanner.nextLine());
			System.out.println("수학 : ");
			int mat = Integer.parseInt(scanner.nextLine());

			int sum = kor + eng + mat;
			avg = sum / 3.0;
			String grade = "F";
	
			switch ((int)(avg/10)) {
			case 10 :
			case 9: grade = "A"; break ;
			case 8: grade = "B"; break ;
			case 7: grade = "C"; break ;
			case 6: grade = "D"; break ;
			default : grade = "F"; break ;
			}

			System.out.println("이름\t국어\t영어\t수학\t총점\t평균\t등급");
			System.out.printf("%s\t%d\t%d\t%d\t%d\t%.2f\t%s\n", name, kor, eng, mat, sum, avg, grade);
			}	
		}while (run);
		System.out.println("종료되었습니다.");
		scanner.close();
	}
	}
```


### 4.2.4 Scanner
- scanner를 사용하려면 import문이 필요하다 : import java.util.Scanner;
- Scanner 객체 생성 : Scanner scanner = new Scanner(System.in);
- 키보드로 입력한 문자열을 얻음 : scanner.nextLine()
- 문자열을 비교할 때는 equals(“”) 메소드 사용


### 4.2.5 break문

- break문은 반복적인 for문 while문 do-while문,  switch문을 실행 중지할 때 사용된다.
- 먄약 반복문이 중첩되어 있을 경우 break문은 가장 가까운 반복문만 종료하고 바깥쪽 반복문은 종료시키지 않는다.
```js
package day9;

import java.util.Scanner;	// Scanner 클래스를 사용하기 위해 필요
public class Break {

	public static void main(String[] args) {

				//boolean run = true;	-- break를 쓰면 run이 필요 없게됨
				Scanner scanner = new Scanner(System.in);	//Scanner 객체 생성
				do {
					String name = "";
					double avg = 0.0;
					System.out.println("-----------------------------------------------");
					System.out.println("이름, 국어, 영어, 수학 점수를 순서대로 입력해주세요[종료:Q]");
					System.out.println("-----------------------------------------------");
					System.out.println("이름[종료:Q]");
					name = scanner.nextLine();//키보드로 입력한 문자열을 얻음
					
					if(name.equals("Q") || name.equals("q")){//문자열을 비교할 때는
															// equals("") 메소드 사용
						System.out.println("종료를 선택했음.");
						break;
						
					} else {
					System.out.println("국어 : ");
					int kor = Integer.parseInt(scanner.nextLine());
					System.out.println("영어 : ");
					int eng = Integer.parseInt(scanner.nextLine());
					System.out.println("수학 : ");
					int mat = Integer.parseInt(scanner.nextLine());

					int sum = kor + eng + mat;
					avg = sum / 3.0;
					String grade = "F";
			
					switch ((int)(avg/10)) {
					case 10 :
					case 9: grade = "A"; break ;
					case 8: grade = "B"; break ;
					case 7: grade = "C"; break ;
					case 6: grade = "D"; break ;
					default : grade = "F"; break ;
					}

					System.out.println("이름\t국어\t영어\t수학\t총점\t평균\t등급");
					System.out.printf("%s\t%d\t%d\t%d\t%d\t%.2f\t%s\n", name, kor, eng, mat, sum, avg, grade);
					}	
				}while (true);
				System.out.println("종료되었습니다.");
				scanner.close();
			}
	}

```
-  1부터 100까지 합을 구하던 중 합이 1000이 넘을 때 정수값 구하기
```js
package day9;

public class Break01 {

	public static void main(String[] args) {
		//1부터 100까지의 합을 출력해주세요
		//1부터 100까지 합을 구하던 중 합이 1000이 넘을 때
		//그때의 정수값을 알고싶어
		int sum = 0 ;
		int i = 0;

		for(i = 1 ; i <= 100 ; i++ ) {
			sum = sum + i ;
			if(sum > 1000) break;
		}
		System.out.println("sum = " + sum);
		System.out.println("1부터 100까지 합 중 1000을 넘을 때 정수"+ i);
	}
}
```

### 4.2.6 Continue문
- continue문은 반복적인 for문, while문, do-while문에서만 사용되는데, 블록 내부에서 continue문이 실행되면 for문의 증감식 또는 while문, do-while문의 조건식으로 이동한다.
```js
package day9;

public class Continue {

	public static void main(String[] args) {
		// 1부터 100까지 6의 배수의 합 출력(continue 사용)
		int sum = 0;
		for(int i = 1 ; i<=100; i++) {
			if(i%6 != 0) {
				continue;
			}
			sum = sum + i ;
		}
		System.out.println("1부터 100까지 6의 배수의 합 = " + sum);
		// 1부터 100까지 6의 배수의 합 = 816
	}

}
```

- 달력 만들기

```js
package day9;

import java.util.Scanner;

public class CalendarMake2 {

	public static void main(String[] args) {
		// 사용자가 요청한 달력생성
		// 고레고리력(양력)
		// 1년 1월 1일 = 월
		// 2년 1월 1일 = 화
		// 3년 1월 1일 = 수
		// 4년 1월 1일 = 목 (4년 2월에 윤년)
		// 5년 1월 1일 = 토
		// (1900 년 1월 1일이 월요일이어서 이곳을 기점으로 하셔도 됩니다.)  
		// 구하는 월의 1일은 무슨 요일이까?
		// 지금까지의 일수를 다 더해서 7로 나눈 나머지 = 시작요일
		
		// 임의의 년도는 윤년인가?
		// 1년은 365일(실제는 365.2) 4년마다 윤년,  100년은 평년, 400년 윤년
		Scanner scanner = new Scanner(System.in);
		System.out.print("년도를 입력 : ");
		int year = Integer.parseInt(scanner.nextLine());
		System.out.print("월을 입력[1~12] : ");
		int month = Integer.parseInt(scanner.nextLine());		
		int lastYear = year - 1;
		
		boolean isLeapYear = false; // 평년 (true : 윤년)		
		// 올해가 윤가/평년 구분
		/* if(year % 400 == 0) {
			isLeapYear = true;
		}else if(year % 100 == 0) {
			isLeapYear = false;
		}else if(year % 4 == 0) {
			isLeapYear = true;
		} */
		
		if((year % 100 != 0 && year % 4 == 0) || (year % 400 == 0)) {
			isLeapYear = true;
		}
		System.out.println(year + "년은 " +  ( isLeapYear ? "윤년" : "평년" ) );
		// 2021년 입력 -> 전년도 까지의 일수 % 7
		// 일수 : (전년도 * 365) + (전년도 까지의 윤년수)
		int totalDay = (lastYear * 365)
				        + (lastYear / 4) + (lastYear / 400) - (lastYear / 100);
		// 해당월 4월1일의 요일을 구하기 위해  (1월 ~ 3월 일수) + 1
		// 구하는 월전까지의 일을 totalDay 에 추가
		for(int i = 1; i < month; i++) {
			if(i == 1 || i == 3 || i == 5 || i == 7 || i == 8 || i == 10 || i == 12 ){
				totalDay = totalDay + 31;
			}else if(i == 2) {
				if(isLeapYear) { // isLeapYear == true
					totalDay = totalDay + 29;
				}else{
					totalDay = totalDay + 28;
				}
			}else {
				totalDay = totalDay + 30;
			}
		}
		// 해당월의 일수 담기
		int lastDay = 30;
		if(month == 1 || month == 3 || month == 5 || month == 7 || month == 8 || month == 10 || month == 12 ){
			lastDay = 31;
		}else if(month == 2) {
			if(isLeapYear) { // isLeapYear == true
				lastDay = 29;
			}else{
				lastDay = 28;
			}
		}		
		
		int dayOfMonth = (totalDay + 1) % 7; // 0 일, 1 월, ~~ 6 토
		System.out.println(totalDay + "=" + totalDay + ", dayOfMonth=" + dayOfMonth);
		
		System.out.println("       " + year + "년 " + month + "월");
		System.out.println("일\t월\t화\t수\t목\t금\t토");
		
		/* // 메인 for 전에 요일만큼 tab 하기
		for(int i = 0; i < dayOfMonth; i++) {
			System.out.printf("\t");
		}		
		//dayofmonth 4 일때  i = 3, 10, 17, ...일에  개행이 필요			
		for(int i = 1; i <= lastDay; i++) {
			System.out.printf("%d\t", i);
			if( (i + dayOfMonth) % 7 == 0) {
				System.out.println();
			}
		}
		*/
		
		// 다르게 for
		// day 일을 출력하가 위한 변수
		for(int i = 1, day = 1; i <= 42; i++) {
			// i 가 dayofMonth 보다 작다면 스킵
			if(i <= dayOfMonth) {
				System.out.print("\t");				
				continue;
			}
			System.out.printf("%d\t", day);
			if( (day + dayOfMonth) % 7 == 0) {
				System.out.println();
			}
			day++;
			// day가 lastDay 보다 크다면 반복문을 빠져나가자
			if(day > lastDay) {
				break;
			}
		}
	}
}
```

# 🐋 Chapter 5
## 📚 5.1 데이터 타입 분류
- 기본 타입
-	 정수타입
      - byte
      - char
       - short
       - int
       - long

-	실수 타입
	- float
	- double

- 참조 타입
	-	배열 타입
	-	열거타입
	-	클래스
    - 인터페이스


## 📚 5.2 메모리 사용 영역
### 5.2.1 메소드 영역
- 메소드 영역에는 코드에서 사용되는 클래스들을 클래스 로더로 읽어 클래스 별로 런타임 상수풀, 핅드 데이터, 메소드 코드, 생성자 코드 등을 분류해서 저장한다.

- 힙 영역
힙 영역은 객체와 배열이 생성되는 영역이다.

- jvm 스택 영역
	- jvm 스택 영역은 각 스레드마다 하나씩 존재하며 스레드가 시작될 때 할당된다. 자바 프로그램에서 추가적으로 스레드를 생성하지 않았다면 main 스레드만 존재하므로 jvm 스택도 하나다.
	- Jvm 스택은 메소드를 호출할 때마다 프레임을 추가하고 메소드가 종료되면 해당 프레임을 제거하는 동작을 수행한다.

## 📚 5.3 참조 변수의 ==,!= 연산

## 📚 5.4 null과 NullpointerException
- 참조 타입 변수는 힙 영역의 객체를 참조하지 않는다는 뜻으로 널값을 가질 수 있다. 
- null값도 초기값으로 사용할 수 있기 때문에 초기화된 참조 변수는 스택 영역에서 생성된다.
- 참조 타입 변수가 null값을 가지는지 확인하려면 ==, != 연산을 수행하면 된다.
> refVar1 == null //결과 : false
> refVar1 != null  // 결과 : true

```js
package day11;

public class Refer01 {

	public static void main(String[] args) {
	
		//기본형은 null 설정 안됨
		//int a = null;
		//char b = null;
		String str = "사랑해요 밀키스";
		System.out.println(str);
		System.out.println("-------------");
		if(str != null) {
			System.out.println(str.length());
		}else {
			System.out.println("str 변수는 널입니다.");
		}
	

	}

}
```

## 📚 5.5 String 타입

- String 변수 ;
- 변수 = “문자열”;
- String 변수 = “문자열”;
- 자바는 문자열 리터럴이 동일하다면 String 객체를 공유하도록 되어 있다.
-하지만 new 연산자를 사용하면 새로운 객체를 만든다.
String name1 = new String (“신용권”)

## 📚 5.6 배열 타입
### 5.6.1 배열이란
- 같은 타입의 많은 양의 데이터를 다루는 프로그렘에서는 좀 더 효율적인 방법이 필요한데 이것이 배열이다.
- 배열의 길이란 배열에 저장할 수 있는 전체 항목 수를 말한다. 코드에서 배열의 길이를 얻으려면 배열 객체의 length 필드를 읽으면 된다. 배열의 length 필드를 읽기 위해서는 배열 변수에 .을 붙이고 length를 적어주면 된다.

```js
package day11;

public class Array01 {

	public static void main(String[] args) {

		int a = 32 ;
		int b = 31 ;
		int c = 35 ;
		int d = 32 ;
		int e = 29 ;
		int f = 26;

		int sum = a + b + c + d ;
		System.out.println("나이의 합  + " sum);
		System.out.println("평균나이" + (sum / 4.0));

	}

}
```
### 5.6.3 값 목록으로 배열 생성

- 데이터 타입 [] 변수 = {값0,  값1, 값2, 값3…}

- 중괄호 {}는 주어진 값들을 항목으로 가지는 배열 객체를 힙에 생성하고 배열 객체의 번지를 리턴한다.
```js
String[] names = {“신용권”, “홍길동”, “감자바”};
```
```js
package day11;

public class Array01 {


	public static void main(String[] args) {
		int[]arr = {32, 31, 35, 32, 29, 26};
		int sum = 0;
		System.out.println("arr[1]= " + arr[1]);
		arr[1] = 55;
		System.out.println("arr.length=" + arr.length);
//		sum += arr{0};
//		sum += arr{1};
//		sum += arr{2};
//		sum += arr{3};
		
		for(int i = 0 ; i < 4; i++) {
			sum = sum + arr[i];
		}
		
		System.out.println("나이의 합" + sum);
		System.out.println("평균 나이" + (sum /(double)arr.length));
	}
}
```

### 5.6.4 new 연산자로 배열 생성
- 값을 목록을 가지고 있지 않지만, 향후 값들을 저장할  배열을 미리 만들고 싶다면 new 연산자로 다음과 같이 배열 객체를 생성시킬 수 있다.
- new 연산자로 배열을 처음 생성할 경우, 배열은 자동적으로 기본값으로 초기화된다.
> 타입[] 변수 = new 타입 [길이];
- ex
```js
int[] intArray = new int[5];
```
```js
package day11;

public class Array01 {

	public static void arr(String[] args) {
		int[]arr = {32, 31, 35, 32, 29, 26};
		int sum = 0;
		System.out.println("arr[1]= " + arr[1]);
		arr[1] = 55;
		System.out.println("arr.length=" + arr.length);

		for(int i = 0 ; i < 4; i++) {
			sum = sum + arr[i];
		}
		sum = add(arr);
		System.out.println("나이의 합" + sum);
		System.out.println("평균 나이" + (sum /(double)arr.length));
		sum = add(new int[] {334, 234, 7655, 7756, 1}) ; //새로 생성하려면 new 붙여라
		System.out.println("sum =" + sum);
	} //main end
	
	//배열을 맏아서 합을 구해서 정수를 리턴하는 함수
	public static int add(int[] ar) {
		int s = 0 ;
		for(int i = 0 ; i <  ar.length ; i++) {
			s = s + ar[1];
			}
		return s ;
		
	}
	
	public static void main(String[] args) {
		// 정수배열 10개 배열을 생성
		int[] arr = new int[10] ;
		int sum = 0 ;
		// 랜덤한 값을 채우고(50부터 100사이)
		// 배열에 있는 모든 값을 출력
		for (int i = 0 ; i < arr.length ; i++ ) {
			arr[i] = (int)(Math.random()*50) +50;	
			System.out.print(arr[i] + " ");
			sum = sum + arr[i] ;  
		}
		// 합계 출력
		// 합계 = 675
		 System.out.println(sum);
		{
		}
	}
}
```

```js
package day12;

public class Array03 {

	public static void main(String[] args) {
		// 정수 배열 10개 배열을 생성
		int[] arr = new int [10];
		int len = arr.length ;
		//랜덤한 값을 채우고 (50부터100 사이)
		for(int i = 0 ; i < len ; i++) {
			arr[i] = (int)(Math.random()* 50) + 50 ;
			
		}
		//배열에 있는 모든 값을 출력
		for(int i = 0 ; i < len; i++) {
			System.out.print(arr[i] + " ") ;
				}
	System.out.println("-------------");
	int maxValue = arr[0]; // 해당 배열의 첫번째값을 초기값으로
	int minValue = arr[0]; // 최대값, 최소값을 구하시오
	
	for(int i = 0 ; i < len ; i ++) {
		if(maxValue < arr[i]) {
			 maxValue = arr[i] ;
		}
		if(minValue > arr[i]){
			minValue = arr[i];
		}  
	}
	
	System.out.println("최대값 : " + maxValue);
	System.out.println("최소값 : " + minValue);
	}
	
	
	
	public static void arr03(String[] args) {
			// 정수 배열 10개 배열을 생성
			int[] arr = new int [10];
			int len = arr.length;
			//랜덤한 값을 채우고 (50부터100 사이)
			for(int i = 0 ; i < arr.length ; i++) {
				arr[i] = (int)(Math.random()* 50) + 50 ;
				
			}
			//배열에 있는 모든 값을 출력
			for(int i = 0 ; i < arr.length ; i++) {
				arr[0] = (int)(Math.random()* 50) + 50 ;
				System.out.println(arr[i] + " ");
		}
			int sum = 0;
			for(int i = 0 ; i < arr.length; i++) {
				sum = sum + arr[i];
				
			}
			System.out.println("합계 = " + sum);
			}
		
			//합계 출력
		
		}
```
### Swap

```js
package day12;

public class Swap01 {

	public static void main(String[] args) {
		int a = 10 ;
		int b = 25 ;
		// a = 25, b = 10으로 swap  하세요
		
		
		int temp;
		temp = a;  // a값을 temp에 옮김
		a = b;		// b값을 a에 옮김
		b = temp ; // temp에 옮겨놨던 a 값을 b에 옮김
		System.out.println(a);	// 25
		System.out.println(b);	// 10
	}

}
```

## 정렬
### 1. 선택정렬
```sql
package day12;

public class SortSelection01 {

	public static void main(String[] args) {
		int[] arr = new int[1000];
		int len = arr.length ;

		for(int i = 0 ; i < len ; i++) {
			arr[i] = (int)(Math.random()* 100) + 1 ;
		}
		//배열에 있는 모든 값을 출력
		for(int i = 0 ; i < len; i++) {
			System.out.print(arr[i] + " ") ;
				}
		System.out.println("\n------------------------");
		for(int i = 0 ; i < (len - 1); i++ ) {
			for(int j = i + 1; j < len; j++) {
				//System.out.println("i = " + i + "j = " + j );
				if(arr[i] > arr[j]) {
					int temp = arr[1] ;
					arr[i] = arr[j] ;
					arr[j] = temp ;
				
				}
				
			}
			System.out.println((i +1) + "Pass Comlete");
		}
		System.out.println("-------------------");
		

	}

}
```
### 2. 버블정렬
```js
package day12;

public class BubbleSort {

	public static void main(String[] args) {
		int[] arr = new int[10];
		int len = arr.length ;

		for(int i = 0 ; i < len ; i++) {
			arr[i] = (int)(Math.random()* 100) + 1 ;
		}
		//배열에 있는 모든 값을 출력
		for(int i = 0 ; i < len; i++) {			
			for (int j = 0; j < len -1 -i  ; j++) {
				System.out.print(j+ arr[j]);
				System.out.println((j+1) + arr[j+1]);
				if(arr[j] > arr[j+1]) {
					int temp = arr[j];
					arr[j] = arr[j+1];
					arr[j+1] = temp ;
					System.out.print(j+ arr[j]);
					System.out.println((j+1) + arr[j+1]);
				}
			}
			System.out.println((i + 1) + "Pass Comlete");		
		}

		for(int i=0; i <len ; i++) {
			System.out.print(arr[i] + " ");
		}
	
	}
}

```
```js
package day12;

public class BreakSort {

	public static void main(String[] args) {
		int[] arr = new int[10];
		int len = arr.length ;

		for(int i = 0 ; i < len ; i++) {
			arr[i] = (int)(Math.random()* 100) + 1 ;
		}
		//배열에 있는 모든 값을 출력
		for(int i = 0 ; i < len; i++) {			
			boolean isSwap = false;
			for (int j = 0; j < len -1 -i  ; j++) {
				
				System.out.print(j+ arr[j]);
				System.out.println((j+1) + arr[j+1]);
				
				
				if(arr[j] > arr[j+1]) {
					int temp = arr[j];
					arr[j] = arr[j+1];
					arr[j+1] = temp ;
					isSwap = true;
					
					System.out.print(j+ arr[j]);
					System.out.println((j+1) + arr[j+1]);
					
				}
			}
			if(isSwap == false) {
				break ;
			}
			System.out.println((i + 1) + "Pass Comlete");		
		
		}

		for(int i=0; i <len ; i++) {
			System.out.print(arr[i] + " ");
		}
	
	}
}


```
```js
public class ar212121 {
	/*
	 * 배열에 두 값을 교환한다.
	 * @param ar int[]형 원본배열
	 * @param x 배열의 index 번호
	 * @param y 배열의 index 번호
	 */
	public static void main(String[] args) {
		// 임의 배열 100개 (1 ~ 100)
		int[] arr = new int[1000];
		int len = arr.length;
		int temp = 0;
		
		for(int i = 0 ; i < len ; i++) {
			arr[i] = (int)(Math.random() * 100) + 1;	// 0.0 <= x < 1.0
		}
		for(int i = 0 ; i < len ; i++) {
			System.out.print(arr[i] + " ");
		}
		
//		System.arraycopy(src, srcPos, dest, destPos, length);
//		int[] arr = Arrays.copyOf(original, newLength);
		int[] arr1 = arr.clone();	// 현재상황을 복제값으로 가져오는것, 원본값 유지
		int[] arr2 = arr.clone();
		
		//Bubble 이 selection 보다 정렬 빠름
		selectionSort(arr1);		// reference 원본값 유지
		for(int i = 0 ; i < len ; i++) {
			System.out.print(arr1[i] + " ");
		}
		System.out.println();
		System.out.println("--------------------------");
		
		bubbleSort(arr2);
		for(int i = 0 ; i < len ; i++) {
			System.out.print(arr2[i] + " ");
		}
	}
	public static void swap(int[] ar, int x, int y) {
		int temp = ar[x];
		ar[x] = ar[y];
		ar[y] = temp;
	}
	public static void selectionSort(int[] arr) {
		long startTime = System.currentTimeMillis();
		boolean isSwap = false;
		int len = arr.length;
		for(int i = 0 ; i < len ; i++) {
			isSwap = false;
			for(int j = 0 ; j < len - 1 - i ; j++) {
				
				if(arr[j] > arr[j+1]) {
					swap(arr, j, j+1);	
					isSwap = true;
				}
			}
			if(!isSwap) {
				break;
			}
		}
		System.out.println("\nselectionSort 소요시간 : " + (System.currentTimeMillis() - startTime));
	}
	
	public static void bubbleSort(int[] arr) {
		long startTime = System.currentTimeMillis();
		int len = arr.length;
		for(int i = 0 ; i < (len - 1) ; i++) {
			for(int j = i + 1 ; j < len ; j++) {
				if(arr[i] > arr[j]) {
					swap(arr, i, j);	
				}				
			}			
		}
		System.out.println("\nbubbleSort 소요시간 : " + (System.currentTimeMillis() - startTime));
	}
}

```

### 5.6.5 커맨드라인 입력
```js
package day14;

public class Array01 {
	public static void main(String[] args) {
		if(args.length !=2) {
			System.out.println("=======================");
			System.out.println("  프로그램 사용법");
	       System.out.println("	example : java day14.Array01 10 100");
	       System.out.println("                 10부터 100까지의 합을 출력");
	       System.out.println("  java day14.array01 10 100");
			System.out.println("=======================");
			//종료
			System.exit(0); //정상적으로 강제 종료 // Runtime.getRuntime().exit(0);과 동일	
		}
		int num1 = Integer.parseInt(args[0]);	//값을 받는 것
		int num2 = Integer.parseInt(args[1]);
		int sum = 0 ;
		
		for(int i = num1 ; i <= num2 ; i++ ) {
			sum = sum + i;
		}
		System.out.println(sum);
		//5부터 99까지의 합은 4940
		
		System.out.println(num1 + "부터" + num2 + "까지의 합은 " +sum);
		//5부터 99까지의 합은 4940
		//run configurations 에서도 실행 가능
		
		
	}

}
```
### 5.6.6 향상된 for 문
```js
package day14;

public class ForEach01 {

	public static void main(String[] args) {
		//원래 for문
		int[] arr = {34, 23 , 5, 90, 1};
		for(int i = 0; i < arr.length; i++) {
			System.out.println((i+1) + "번째 =" + arr[i]);
		}
		System.out.println("\n-----------------");
		
		//향상된 for문
		int i = 1;
		for(int x : arr) {
			System.out.println(i  + "번째 = " + x );
			i++;
		}
	}
}
```

- 로또
```js
package day14;

import java.util.Scanner;

public class Lott03 {

	public static void main(String[] args) {
		// 사용자로부터 숫자 6개를 입력받아서(입력한 숫자는 모두 다르다고 가정함)
		// 두배열(lotto, user)을 비교해 매칭된 건수 저장
		// 로또번호 : 17 34 41 4 32 40
		// 입력번호 : 25 41 4 31 27 17
		// 3개 미만이면 다음 기회에
		// 3개면 "당첨되었습니다. 5,000원"
		// 4개면 "당첨되었습니다. 50,000원"
		// 5개면 "당첨되었습니다. 총 매출금액의 12.5%를 지급합니다."
		// 6개면 "당첨되었습니다. 총 매출금액의 75%를 지급합니다."

		System.out.print("로또번호 : ");
		int[] lotto = new int[6];
		int len = lotto.length;

		for (int i = 0; i < len; i++) {
			lotto[i] = (int) ((Math.random() * 10) + 1);
			for (int j = 0; j < i; j++) {
				if (lotto[i] == lotto[j]) {
					i--;
					break;
				}
			}
		}
		for (int i = 0; i < len; i++) {
			System.out.print(lotto[i] + " ");
		}

		System.out.println();
		System.out.print("입력번호 : ");

		int[] user = new int[6];
		int us = user.length;
		int k = 0 ;
		Scanner scanner = new Scanner(System.in);
		System.out.println("번호 6개를 입력하세요");
		for(k = 0 ; k < len ; k++) {
			user[k] = scanner.nextInt();
		}
		
		System.out.print("입력번호 : ");
		
		for(k = 0 ; k < len ; k++) {
			System.out.print(user[k]+ " ");
		}
		scanner.close();
		
		int count = 0;
		for (int i = 0; i < len; i++) {
			for (int j = 0; j < us; j++) {
				if (lotto[i] == user[j]) {
					count++;
					break;
				}
			}
		}
		
		System.out.println("");
		if (count < 3) {
			System.out.println("낙첨되었습니다");

		} else if (count == 3) {
			System.out.println("당첨되었습니다. 5,000원");
		} else if (count == 4) {
			System.out.println("당첨되었습니다. 50,000원");
		} else if (count == 5) {
			System.out.println("당첨되었습니다. 총 매출금액의 12.5%를 지급합니다.");
		} else {
			System.out.println("당첨되었습니다. 총 매출금액의 75%를 지급합니다.");
		}
		System.out.println(count);
	}
}
```
### 5.6.7 배열
- 성적표 만들기
```js
package day14;

 import java.util.Scanner;

public class MultiArray {

	public static void main(String[] args) {
		int cnt = 2; //학생수
		String[] names = new String[cnt] ;
		int[][] scores = new int[cnt][4];
		double[] avg = new double[cnt] ;
		Scanner sc = new Scanner(System.in);
		for(int i = 0 ; i < names.length; i++) {
			System.out.print("학생이름 : " );
			names[i] = sc.nextLine();
			System.out.print("국어 점수 : ");
			scores[i][0] = sc.nextInt();	
			System.out.print("영어 점수 : ");
			scores[i][1] = sc.nextInt();
			System.out.print("수학 점수 : ");
			scores[i][2] = sc.nextInt();
			sc.nextLine() ;
			//총점 및 평균
			scores[i][3] = scores[i][0] + scores[i][1] +scores[i][2] ;
			avg[i] = scores[i][3] / 3.0 ;
		}
		//학생 점수 출력
		System.out.println("=====================");
		System.out.println("       성적표           ");
		System.out.println("=====================");
		System.out.println("성명\t국어\t영어\t수학\t총점\t평균\t");
		for(int i = 0; i < cnt ; i++) {
			System.out.print(names[i] + "\t");
			System.out.print(scores[i][0] + "\t");
			System.out.print(scores[i][1] + "\t");
			System.out.print(scores[i][2] + "\t");
			System.out.print(scores[i][3] + "\t");
			System.out.print(avg[i] + "\n");
		}
		sc.close();
		
	}

//	학생이름 : 사승원
//	국어 점수 : 88
//	영어 점수 : 88
//	수학 점수 : 88
//	학생이름 : 사승원
//	국어 점수 : 77
//	영어 점수 : 77
//	수학 점수 : 77
//	=====================
//	       성적표           
//	=====================
//	성명	국어	영어	수학	총점	평균	
//	사승원	88	88	88	264	88.0
//	사승원	77	77	77	231	77.0

```

- 성적표 만들기2(for)
```js
package day14;

 import java.util.Scanner;

public class MultiArray {

	public static void main(String[] args) {
	// String[]name = new String[cnt];
		String[] names = {"밀키스", "말자", "순자"};
		String[] subjects = {"국어", "영어", "수학"};
		
		int sum = 0;
		int cnt = names.length; //학생수
		int[][] scores = new int[cnt][4];
		double[] avg = new double[cnt] ;
		Scanner sc = new Scanner(System.in);
		for(int i = 0 ; i < names.length; i++) {
			//밀키스 님의 성적을 등록해주세요
			System.out.println(names[i] + "님의 성적을 등록해주세요");
			//scores[i][0] = sc.nextInt();
			//교과목을 위 subjects 배열을 사용해서 입력
			for(int j = 0; j < subjects.length ; j++) {
				System.out.println(subjects[j] + "점수 : ");
				scores[i][j] = sc.nextInt();
				//sum = scores[0][4];
				}
			//각 과목의 점수를 입력 받으면 그 사람의 총점에 누적
			scores[i][3] = scores[i][0] + scores[i][1] +scores[i][2] ;
			avg[i] = scores[i][3] / 3.0 ;
		}
		//학생 점수 출력
		System.out.println("========================================");
		System.out.println("     		  성적표			       ");
		System.out.println("========================================");
		System.out.println("성명\t국어\t영어\t수학\t총점\t평균\t");
		for(int i = 0; i < cnt ; i++) {
			System.out.print(names[i] + "\t");
			// 각 점수 및 총점은 score 배열 사용해서 출력
			for(int j = 0 ; j < subjects.length ; j++ ) {
			System.out.print(scores[i][j] + "\t");
		}
			System.out.print(scores[i][3] + "\t");
			System.out.println(avg[i]);
		}
		sc.close();
		
	}
}

//	밀키스님의 성적을 등록해주세요
//	국어점수 :
//	90
//	영어점수 :
//	90
//	수학점수 :
//	90
//	말자님의 성적을 등록해주세요
//	국어점수 :
//	80
//	영어점수 :
//	80
//	수학점수 :
//	80
//	순자님의 성적을 등록해주세요
//	국어점수 :
//	70
//	영어점수 :
//	70
//	수학점수 :
//	70
//	========================================
//	     		  성적표			       
//	========================================
//	성명	국어	영어	수학	총점	평균	
//	밀키스	90	90	90	270	90.0
//	말자	80	80	80	240	80.0
//	순자	70	70	70	210	70.0
```


- 성적표 만들기3
```js
package day14;

 import java.util.Scanner;

public class MultiArray {

	public static void main(String[] args) {
	// String[]name = new String[cnt];
		String[] names = {"밀키스", "말자", "순자"};
		String[] subjects = {"국어", "영어", "수학"};
		
		int sum = 0;
		int cnt = names.length; //학생수
		int[][] scores = new int[cnt][subjects.length + 1]; //int[여기는 cnt(3)][여기는4(국어,영어,수학+총점이라서 4)]
		double[] avg = new double[cnt] ;  // 세 명의 평균이 다 필요해서
		Scanner sc = new Scanner(System.in);
		for(int i = 0 ; i < names.length; i++) {
			//밀키스 님의 성적을 등록해주세요
			System.out.println(names[i] + "님의 성적을 등록해주세요");
			//scores[i][0] = sc.nextInt();
			//교과목을 위 subjects 배열을 사용해서 입력
			for(int j = 0; j < subjects.length ; j++) {
				System.out.println(subjects[j] + "점수 : ");
				scores[i][j] = sc.nextInt();
				scores[i][subjects.length] = scores[i][subjects.length] + scores[i][j] ;
				//sum = scores[0][4];
				}
			//각 과목의 점수를 입력 받으면 그 사람의 총점에 누적	
			avg[i] = scores[i][3] / 3.0 ;
		}
		//학생 점수 출력
		System.out.println("========================================");
		System.out.println("     		  성적표			       ");
		System.out.println("========================================");
		System.out.println("성명\t국어\t영어\t수학\t총점\t평균\t");
		for(int i = 0; i < cnt ; i++) {
			System.out.print(names[i] + "\t");
			// 각 점수 및 총점은 score 배열 사용해서 출력
			for(int j = 0 ; j < scores[i].length ; j++ ) { // scores[i].length : 뒤에 배열 가져오기
			System.out.print(scores[i][j] + "\t");
		}
			System.out.println(avg[i]);
		}
		sc.close();
		
	}
}

//	밀키스님의 성적을 등록해주세요
//	국어점수 :
//	90
//	영어점수 :
//	90
//	수학점수 :
//	90
//	말자님의 성적을 등록해주세요
//	국어점수 :
//	80
//	영어점수 :
//	80
//	수학점수 :
//	80
//	순자님의 성적을 등록해주세요
//	국어점수 :
//	70
//	영어점수 :
//	70
//	수학점수 :
//	70
//	========================================
//	     		  성적표			       
//	========================================
//	성명	국어	영어	수학	총점	평균	
//	밀키스	90	90	90	270	90.0
//	말자	80	80	80	240	80.0
//	순자	70	70	70	210	70.0

```



### 상수 선언
```js
package day15;

public class Enum02 {
	//상수 정적(static final) 선언 대문자, 언더바 (관례)
	//상수를 사용해 알아보기 쉽게 바꿀 수 있음
	public static final int CALC_ADD = 1;
	public static final int CALC_SUBTRACTION = 2;
	public static final int CALC_MULTIPLE = 3;
	public static final int CALC_DEVIDE = 4;
	
	
	public static void main(String[] args) {
		System.out.println("CALC_ADD = " + CALC_ADD);
		// 상수는 값을 할당 못함 //CALC_ADD = 1
		
				int a = 10;
				int b = 3;
				System.out.println("calc(a, b, 1)= " + calc(a, b, CALC_ADD));	//calc(a, b, 1)= 13
				System.out.println("calc(a, b, 1)= " + calc(a, b, CALC_SUBTRACTION));	//calc(a, b, 1)= 7
				System.out.println("calc(a, b, 1)= " + calc(a, b, CALC_MULTIPLE));	//calc(a, b, 1)= 30
				System.out.println("calc(a, b, 1)= " + calc(a, b, CALC_DEVIDE));	//calc(a, b, 1)= 3
				System.out.println("---------------------");
				System.out.println();

			}

			// 두 숫자 하고 계산방식에 연산 결과 리턴함수
			public static int calc(int x, int y, int what) {
				int res = 0;
				if(what == CALC_ADD) {
					res = x + y;
				}else if (what == CALC_SUBTRACTION) {
					res = x - y ;
				}else if (what == 3 ) { //상수로 해도됨 CALC_MULTIPLE
					res = x * y ;
				}else {
					res = x / y;
				}
				return res;
			}
	}

```


```js
package day15;


		public class Calc00 {
			//상수 정적(static final) 선언 대문자, 언더바 (관례)
			//상수를 사용해 알아보기 쉽게 바꿀 수 있음
			public static final int CALC_ADD = 1;
			public static final int CALC_SUBTRACTION = 2;
			public static final int CALC_MULTIPLE = 3;
			public static final int CALC_DEVIDE = 4;
			
			
			public static void main(String[] args) {
						int a = 10;
						int b = 3;
						Calc c = Calc.ADD ;
						System.out.println(calc(a,b,c));
						c= Calc.SUBTRACTION;
						
						
						System.out.println("calc(a, b, ADD)= " + calc(a, b, Calc.ADD));	//calc(a, b, ADD)= 13
						System.out.println("calc(a, b, SUBTRACTION)= " + calc(a, b, Calc.SUBTRACTION));	//calc(a, b, SUBTRACTION)= 7
						System.out.println("calc(a, b, MULTIPLE)= " + calc(a, b, Calc.MULTIPLE));	//calc(a, b, MULTIPLE)= 30
						System.out.println("calc(a, b, DEVIDE)= " + calc(a, b, Calc.DEVIDE));	//calc(a, b, DEVIDE)= 3
						System.out.println("---------------------");

					}

					// 두 숫자 하고 계산방식에 연산 결과 리턴함수
			public static int calc(int x, int y, Calc what) {
				int res = 0;
				if(what == Calc.ADD) {
					res = x + y;
				}else if (what == Calc.SUBTRACTION) {
					res = x - y ;
				}else if (what == Calc.MULTIPLE ) { //상수로 해도됨 CALC_MULTIPLE
					res = x * y ;
				}else {
					res = x / y;
				}
				return res;
					}
	}
```
```js
package day15;

public enum Calc {//class로 생성해도 나중에 enum으로 바꿔주면 됨
	ADD,
	SUBTRACTION,
	MULTIPLE,
	DEVIDE
}
```
- enum 
```js
package day15;

public class MyLove {
	//이곳에 문자열 상수 LOVE_NAME에 "말자"를 설정해서 변경해주세요
	//프로그램에서 반복적으로 사용되며, 변하지 않는 값을 지정
	//차후 변경이 발생하더라도 쉽게 변경 가능하려면 상수로 지정하자
	//대표적인 상수 = 파이 : "3.141592....
	public static final String LOVE_NAME = "말자";	//때에 따라 ""사이 값을 바꿀 수 있음
	public static final double PI = 3.141592 ;
	//상수는 고유한 값을 가질 수 있어요
	//하지만 enum은 안돼요...
	
	public static void main(String[] args) {
		//A 클라이언트에게 납품...(말자)
		Calc c = Calc.MULTIPLE;
		System.out.println("c = " + c);
		System.out.println("name() = " + c.name());
		System.out.println("ordinal() = " + c.ordinal());
		System.out.println("compareTo() = " + c.compareTo(Calc.ADD));
		Calc[] ces = c.values();
		for(Calc x : ces) {
			System.out.println(x);
		}
		
		
		System.out.println("내 첫사랑은 " + LOVE_NAME +"였어요");
		//B 클라이언트는 "순자"
		System.out.println(LOVE_NAME);
		
	    //"사랑해요 말자" 를 3번 출력
		lovePrint(3);
	
		System.out.println("-------------");
		//"사랑해요 말자" 를 5번 출력
		lovePrint(5);
	}
	
	public static void lovePrint(int cnt) {
		for(int i = 0; i < cnt; i++) {
			System.out.println("사랑해요 말자");
		}
	}
}
```

# 🐋 Chapter 6 클래스 

## 6 클래스
기계어 : 시스템에서 실행가능코드
어셈블리어 : 기계어와 일대일 대응이 되는 컴퓨터 프로그래밍의 저급 언어
절차형 언어 : 절차지향 프로그래밍 패러다임의 일종으로서,
			프로시저 호출의 개념을 바탕으로 하고있는 프로그래밍 패러다임
			프로시저는 루틴, 하위프로그램, 서브루틴, 메서드, 함수
			함수기반의 프로그램(C, 코볼, 파스칼, 포트)
			
- 객체지향프로그래밍(OOP:Object Oriented Programming)
  : 하나하나의 독립된 "객체"들의 그룹으로 생각하면 되고,
  	객체간의 메시지를 주고 받음으로서 쉽게 연결이 가능하다.
  	
- 관점지향프로그래밍(AOP : Aspect Oriented Programming)
  : 객체지향적으로 프로그래밍을 구성하여도 실제 코드는 중복된 코드가 발생합니다.  
  	- Core concern(핵심관심사) : 실제 해야할 일
  	- Cross-cutting Concern(횡단관심사) : 부수적인 일, 하지만 꼭 해야하는 일
 1000라인의 코드가 있는데 이중 핵심관심사 200라인도 안됨
 나머지 800라인은 로깅처리, 트랜잭션관리, 권한체크 등 횡단관심이 존재한다.
 - 소스의 가독성이 좋아지고 개발자는 핵심로직에 집중하여 양질의 sw가 만들어짐.
 AOP는 횡단관심사를 별도의 클래스로 분리해서 작성하고, 실제 실행될 때는 (핵심관심사 + 횡단관심사) 합쳐져서 원래의 의도대로 동작하게 하는 프로그램 기법
  	
- OOP에서 부족한 부분을 AOP 통해서 보조할 수 있다.
  
  	
  
 #### 1. 객체지향언어의 특징
 	- 캡슐화(Encapsulation)
 	  데이터와 코드의 형태를 외부로부터 알 수 없게 하고,
 	  데이터의 구조와 역할, 기능을 하나의 캡슐형태로 만드는 방법이다.
 	  멤버(필드,메서드)를 숨길것인지, 노출할 것인지를 접근제한자(public, private, default, protected)로 구현
 	  
 	- 상속(Inheritance)
 	  상위 클래스의 모든걸 하위 클래스가 모두 이어 받는 것
 	  즉, 부모 클래스가 자식에게 유전자를 물려주듯 부모의 특징을 자식에게 모두 물려준다.
 	  상위클래스를 잘 구성하면 여러 하위 클래스 생성시 효율적이고 개발시간 단축
 	  상위클래스를 변경하면 모든 하위클래스에 전파되어 유지보수 시간 단축
 	  
 	- 다형성(Polymorphism)
 	  상속과 연관이 있는 개념으로 한 객체가 다른 여러형태(객체)로 재구성 되는 것을 말한다.
 	  쉽게 말해 한 부모의 밑에서 태어난 자식이 똑같지 않은 것과 같은 것
 	  자바의 오버로드 또는 오버라이드가 다형성의 대표적인 예라고 할 수 있고,
 	  이것을 구현하는 걸 오버로딩과 오버라이딩이라고 한다.
 	  - Over-loading : 동일한 메서드지만, 상황에 따라 다른 연산을 수행
 	  	(예 swp(int, int), swap(Student, Student), swap(int[], int, int))
 	  - Over-riding : 부모의 기능을 확장하는 방법 (재정의)
 	 - 추상화(Abstraction)
 	  - 객체의 공통적인 속성과 기능을 추출하여 정의하는 것을 말한다.
 	  	다시 말하면 실제로 존재하는 객체들을 프로그램으로 만들기 위한 공통적인 특성을 파악해
 	  	필요없는 특성을 제거하는 과정을 말함
 	  	
 	  	
#### 2. 객체지향 언어의 장점
 	 1. 재사용성 : 상속을 통해 프로그래밍 시 코드의 재사용을 높일 수 있음
 	 2. 생산성 향상 : 잘 설계된 클래스를 만들어서 독립적인 객체를 사용함으로써 개발의 생산성을 향상시킬 수 있음.   	
 	 3. 자연적인 모델링 : 우리 일상생활의 모습의 구조가 객체에 자연스럽게 녹아들어 있기 때문에 생각하고 있는 것을 그대로 자연스럽게 구현할 수 있다.
	 4. 유지보수의 우수성 : 프로그램 수정시 추가, 수정을 하더라도 캡슐화를 통해 주변 영향이 적기때문에 유지보수가 쉬워서 매우 경제적이라할 수 있다. 	
 	  	
 	  	
 #### 3. 객체지향 언어의 단점
 	 1. 개발속도가 느린점 : 객체가 처리하려는 것에 대한 정확한 이해가 필요하기에 설계단계부터 많은 시간이 소모 된다.
	 2. 실행속도가 느린점 : 객체지향언어는 대체적으로 실행속도가 느리다.
	 3. 코딩난이도 상승 : 다중 상속이 지원되는 C++ 같은 경우에 너무 복잡해져 코딩의 난이도가 상승할 수 있다.
	
#### 4. 표기법
- 클래스 : 대문자 시작, StudentManager : 낙타식 표기법
- 메서드, 필드 : 소문자 시작, addStudent : 낙타식 표기법
- 상수 : 문자 : CALC_DEVIDE : 헝가리언 표기법
- (memName (낙타식), str_mem_name(헝가리언))
									
클래스 파일에 여러 클래스 선언 가능
소스파일과 동일한 클래스에만 public 사용 가능
단, public 사용 안 됨
관례적으로 한 파일에 한 클래스만 정의 하자 	

## 📚 6.1 Class의 용도
- 데이터 저장
- 기능(함수, 조작)

```js

package day15;

import java.util.Calendar;

public class Calendar01 {

	public static void main(String[] args) {
		//Calendar 클래스
		//LocalDateTime (JDK 8)
		//현재 시간으로 설정
		Calendar cal = Calendar.getInstance();
		System.out.println(cal.get(Calendar.YEAR)); // 1 = YEAR  2021
		System.out.println(cal.get(1)); // 1 = YEAR	2021
		System.out.println(cal.get(Calendar.MONTH) + 1); // 2 = MONTH
		System.out.println(cal.get(Calendar.DAY_OF_MONTH));
		System.out.println(cal.get(Calendar.DAY_OF_WEEK)); //1:일 ~ 토(7)  오늘 월요일 : 2
		System.out.println(cal.get(Calendar.DAY_OF_YEAR)); 	
		
		//4월로 변경
		cal.set(Calendar.MONTH, 3); //4월을 하려면 3으로 입력
		System.out.println(cal.get(Calendar.DAY_OF_MONTH));
		System.out.println(cal.get(Calendar.DAY_OF_YEAR));
		System.out.println(cal.get(Calendar.DAY_OF_MONTH));
	}
}

```
### java.time

- java.time 패키지의 핵심 클래스
- 날짜와 시간을 하나로 표현하는 Calendar클래스와 달리,
- java.time 패키지에서는 날짜와 시간을 별도의 클래스로 분리해 놓았다.
- 시간을 표현할 때는 LocalTime 클래스를 사용하고,
- 날짜를 표현할 때는 LocalDate클래스를 사용한다.
- 그리고 날짜와 시간이 모두 필요할 때는 LocalDateTime클래스를 사용하면 된다.
- 만약 여기에 Time-Zone까지 다뤄야 한다면, ZonedDateTime클래스를 사용한다.
```js
package day15;

import java.time.LocalDate;
import java.time.LocalDateTime;
import java.time.LocalTime;
import java.util.Date ;
import java.util.TimeZone;

public class LocalDate01 {

	public static void main(String[] args) {
		//LocalDate
		LocalDate date = LocalDate.now();
		System.out.println(date);
		date = LocalDate.of(2021, 4, 24);
		System.out.println(date);
		System.out.println(date.getYear() + "/" + date.getMonth() + "/" + date.getDayOfYear());
		
		// 로컬 컴퓨터의 현재 시간 정보를 저장한 LocalDate 객체를 리턴.
		LocalTime currentTime = LocalTime.now();   

		// 파라미터로 주어진 시간 정보를 저장한 LocalTime 객체를 리턴.
		LocalTime targetTime = LocalTime.of(12,33,35,22);
		// 끝에 4번째 매개변수는 nanoSecond 인데 선택 값이다 굳이 쓰지 않아도 된다.
		// 결과 : 12:32:33.0000022
		
		// 로컬 컴퓨터의 현재 날짜와 시간 정보
		LocalDateTime currentDateTime = LocalDateTime.now();    
		// 결과 : 2019-11-12T16:34:30.388

		LocalDateTime targetDateTime = LocalDateTime.of(2019, 11, 12, 12, 32,22,3333);
		// 여기도 second,nanoSecond 매개변수는 필수가 아닌 선택입니다.
		// 결과 : 2019-11-12T12:32:22.000003333	
	}
}
```
- 성적표
```js

package day15;

import java.util.Scanner;

public class StudentManager {
	//학생 3명
	private Student[] students = new Student[3] ;
	private int curIdx = 0;
	
	//학생 추가 메서드
	//void method() : 파라미터 X , 반환 X
	//void method(파라미터....) : 파라미터 O , 반환 X
	//type method() : 파라미터 X , 반환 O
	//type method(파라미터....) : 파라미터 O , 반환 O
	public void addStudent() {
		// curidx > 2 이면 안돼요.
		if(curIdx > 2 ) {
			System.out.println("학생이 이미 꽉 차있어요...");
			return ; //현재의 메서드를 빠져나간다. return 타입에 따라서 값 리턴
		}
		Scanner sc = new Scanner(System.in);
		//학생 객체 생성
		
		Student stu = new Student ();
		System.out.println("stu.hashcode = " + stu.hashCode() );
		System.out.print("학생 이름 : " );
		stu.name = sc.nextLine();
		System.out.print("국어 점수 : " );
		stu.kor = Integer.parseInt(sc.nextLine());
		System.out.print("수학 점수 : " );
		stu.mat = Integer.parseInt(sc.nextLine());
		System.out.print("영어 점수 : " );
		stu.eng = Integer.parseInt(sc.nextLine());
		
		stu.total = stu.kor + stu.mat + stu.eng ;
		stu.avg = (double)stu.total / 3;
		students[curIdx] = stu ;
		curIdx++;
		//sc.close();
	}

	//등수처리 메서드
	public void rankProc() {
		//내 점수가 낮다면 rank 를 ++
		
	}
	
	//학생점수 출력

	public void viewStudent() {
		System.out.println("=====================");
		System.out.println("       성적표           ");
		System.out.println("=====================");
		System.out.println("성명\t국어\t영어\t수학\t총점\t평균\t등수");
		for(int i = 0; i < students.length ; i++) {
			Student vo = students[i];
			System.out.print(vo.name + "\t");
			System.out.print(vo.kor + "\t");
			System.out.print(vo.mat + "\t");
			System.out.print(vo.eng + "\t");
			System.out.print(vo.total + "\t");
			System.out.print(vo.avg + "\t");
			System.out.print(vo.rank + "\n");
		}
	}
	
}

```
```js
package day15;

public class Student {
	
	//클래스는 대문자로(관례)
	//한글/영어는 상관 없지만 한글로 만드는 경우는 거의 없다.
	public String name ;
	public int kor ;
	public int eng ;
	public int mat ;
	public int total ;
	public double avg ;
	public int birthYear;
	
	//과제
	public int rank = 1 ;
```

```js

package day15;

public class StudentTest {

	public static void main(String[] args) {
		StudentManager sm = new StudentManager();
		sm.addStudent();
		System.out.println("1------------------");
		sm.addStudent();
		System.out.println("2------------------");
		sm.addStudent();
		System.out.println("3------------------");
		sm.addStudent();
		System.out.println("------------------");
		sm.viewStudent();
		sm.rankProc();
		sm.viewStudent();
		}
}

```
- 학생 이름과 점수 받아서 순위 매기기

```js
//성적표 출력(순위)
package day15;

import java.util.Scanner;

public class StudentManager {
	//학생 3명
	private Student[] students = new Student[3] ;
	private int curIdx = 0;
	
	//학생 추가 메서드
	//void method() : 파라미터 X , 반환 X
	//void method(파라미터....) : 파라미터 O , 반환 X
	//type method() : 파라미터 X , 반환 O
	//type method(파라미터....) : 파라미터 O , 반환 O
	public void addStudent() {
		// curidx > 2 이면 안돼요.
		if(curIdx > 2 ) {
			System.out.println("학생이 이미 꽉 차있어요...");
			return ; //현재의 메서드를 빠져나간다. return 타입에 따라서 값 리턴
		}
		Scanner sc = new Scanner(System.in);
		//학생 객체 생성
		
		Student stu = new Student ();
		System.out.println("stu.hashcode = " + stu.hashCode() );
		System.out.print("학생 이름 : " );
		stu.name = sc.nextLine();
		System.out.print("국어 점수 : " );
		stu.kor = Integer.parseInt(sc.nextLine());
		System.out.print("수학 점수 : " );
		stu.mat = Integer.parseInt(sc.nextLine());
		System.out.print("영어 점수 : " );
		stu.eng = Integer.parseInt(sc.nextLine());
		
		stu.total = stu.kor + stu.mat + stu.eng ;
		stu.avg = (double)stu.total / 3;
		students[curIdx] = stu ;
		curIdx++;
		//sc.close();
	}

	//등수처리 메서드
	public void rankProc() {
		int len = students.length;
		for(int i = 0 ; i < len -1 ; i++) {
			for(int j = 0 ; j < len ; j++) {
				if(students[i].total < students[j].total ) {
					Student temp = students[i] ;
					students[i] = students[j];
					students[j] = temp;
					
				}//for j
			}//for i
			students[i].rank = (i + 1);
		}
		students[len-1].rank = len;
		}
		
		//내 점수가 낮다면 rank 를 ++
		
	
	
	//학생점수 출력

	public void viewStudent() {
		System.out.println("=====================");
		System.out.println("       성적표           ");
		System.out.println("=====================");
		System.out.println("성명\t국어\t영어\t수학\t총점\t평균\t등수");
		for(int i = 0; i < students.length ; i++) {
			Student vo = students[i];
			System.out.print(vo.name + "\t");
			System.out.print(vo.kor + "\t");
			System.out.print(vo.mat + "\t");
			System.out.print(vo.eng + "\t");
			System.out.print(vo.total + "\t");
			System.out.print(vo.avg + "\t");
			System.out.print(vo.rank + "\n");
		}
	}
	
}
```


	
### 6.7 생성자
생성자는 new 연산자와 같이 사용되어 클래스로부터 객체를 생성할 때 호출되어 객체의 초기화를 담당한다. 객체 초기화란 필드를 초기화하거나, 메소드를 호출해서 객체를 사용할 준비를 하는 것을 말한다. 생성자를 실행시키지 않고는 클래스로부터 객체를 만들 수 없다.

#### 6.7.1 기본 생성자
클래스가 public class로 선언되면 기본 생성자에서도 public이 붙지만, 클래스가 public 없이 class로만 선언되면 기본 생성자에도 public이 붙지 않는다.
그렇기 때문에 클래스에 생성자를 선언하지 않아도 다음과 같이 new 연산자 뒤에 기본 생성자를 호출해서 객체를 생성시킬 수 있다.
그러나 클래스에 명시적으로 선언한 생성자가 한 개라도 있으면, 컴파일러는 기본 생성자를 추가하지 않는다.

#### 6.7.2 생성자 선언
생성자는 메소드와 비슷한 모양이지만, 리턴 타입이 없고 클래스 이름과 동일하다.

#### 6.7.3 필드 초기화
매개 변수의 이름이 너무 짧으면 코드의 가독성이 좋지 않기 때문에 가능하면 초기화시킬 필드 이름과 비슷하거나 동일한 이름을 사용할 것을 권한다.관례적으로 필드와 동일한 이름을 갖는 매개 변수를 사용한다. 이 경우 필드와 매개 변수 이름이 동일하기 때문에 생성자 내부에서 해당 필드에 접근할 수 없다. 왜냐하면 동일한 이름의 매개 변수가 사용 우선순위가 높기 때문이다. 해결 방법은 필드 앞에 this 를 붙이면 된다.





```js
package day17;

import day15.Student;

public class Member {


		//이름, 아이디, 마일리지, Student
		String memId;
		String memName;
		int memMileage;
		Student student;
		
	// 생성자 명시적으로 존재하지 않으면 컴파일러가 기본 생성자를 생성합니다.
	// public Member(){}
	// 만약 하나라도 생성자가 있다면, 기본 생성자는 생성되지 않아요. 필요하다면 직접 구현
		
		Member(String memId, String memName, int memMileage) {
			this(memId, memName, memMileage, null);
			
			
		}
		//public Member(String a, String a) {} 매개변수의 타입과 개수 그리고 선언된 순서가 같을 경우 매개 변수 이름만 바꾸는 것은 생성자 오버로딩이라고 볼 수 없다.(타입이 다르면 가능)
													// 생성자 오버로딩이란 매개 변수를 달리하는 생성자를 여러 개 선언하는 것을 말한다.
		   Member (String memId, String memName, int memMileage, Student student ) {
		
			// memId = id; 변수를 검색할 때 지역(매개)변수가 우선순위가 높다.
			this.memId = memId ; // 객체 자신을 뜻하는 this를 사용해야 한다.
			this.memName = memName ;
			this.memMileage = memMileage ;
			student = new Student() ;
			student.name = memName ;
			
		

	//	Member(String memId, String memName, int memMileage){
			
			this.memId = memId;
			this.memName = memName ;
			this.memMileage = memMileage ;
			this.student = student ;
			
		}
}

```

```js
package day17;

import day15.Student;

public class MemberTest {

	public static void main(String[] args) {
		int[] arr = {12, 34, 34, 45, 67, 99};
		display(2);
		display(2, 34);
		display(2, 34, 56);
		int r = display(2, 34, 56);
		System.out.println("r = " + r);
		display(arr);
	}
	public static int display(int...a) { //void : 리턴할 게 없다. //int로 리턴하겠다. new int[3] ={2, 34, 56}
		int s = 0;
		//내부적으로 배열입니다.
		for(int i = 0 ; i < a.length ; i++ ) {
			System.out.printf("%3d" , a[i]);
			s = s + a[i];
		}
		
		System.out.println();
		return s;	//return하려면 void X
		
//		  2
//		  2 34
//		  2 34 56
//		 12 34 34 45 67 99
	}
	
//	public static void displayArray(int[] a) {
//		for (int i = 0 ; i < a.length ; i++ ) {
//			System.out.printf("%3d, a[i]");
//		}
//		
//	}
	
	public static void main2(String[] args) {
		Member m1 = new Member("b001", "이쁜이",23); //Member class에서 생성자를 가져온다.
		//Member m2 = new Member();
		
		System.out.println(m1.memId);
		System.out.println(m1.memName);
		System.out.println(m1.memMileage);
		System.out.println(m1.student);
		m1.memId = "a001" ;
		m1.memName = "김은대";
		m1.student = new Student() ;
		//System.out.println(a); // 일반변수는 초기화가 꼭 필요
		System.out.println(m1.memId);
		System.out.println(m1.memName);
		System.out.println(m1.memMileage);
		System.out.println(m1.student);
	}

}

```
- 정적 멤버(필드, 메서드)는 클래스 로딩시 메서드 영역에 바로 생성된다.
- 그래서 객체 생성 없이 바로 사용 가능하다.

- 정적 멤버(필드, 메서드)를 객체에서 접근가능하지만 오해의 소지가 있으므로 클래스로 접근하는 것을 권장합니다.
```sql
Student
StudentManager
	+ rankProc(Student...) : 랭크 설정
	+ viewStudent(Student...) : 학생들의 정보를 출력
```
- 위 rankProc, vieStudent 는 StudentManager 객체의 필드를 사용하지 않고 단순한 기능만 한다.
- 정적 메서드로 구성해서 작업

- 정적메서드는 객체 생성 없이 바로 사용 가능한데..어떤 사용자(개발자)가 StudentManager를 생성해서 사용하는 일 발생
- 객체를 한 개만 생성해서 사용해도 되는데 매번 객체를 생성하면 메모리낭비가 생긴다.
- 그래서 여러 방법이 생겨났는데 그중 가장 효율적인 방법이 나타났다.(best practice)

- 싱글턴 패턴 : 객체를 하나만 생성 하도록 하며, 생성된 객체를 어디에서든지 참조할 수 있도록 하는 패턴 ex) new xxx() 불가능하게 막음
  1. 생성자를 Private로 만들어서 막음
  2. 정적 클래스 변수 생성
  3. 정적변수를 리턴하는 메서드 생성
			
- 객체 생성은 클래스 내부에서 한다.
- 디자인 패턴 : 프로그램 개발 시에 자주 부딪히는 애로 상황에 대한 일반적이고 재사용 가능한 추상화된 해결책이다.
이런 해결책들은 일반적인 문제를 해결하기 위한 Best practice를 어느 정도 공식화하고 정의했다고도 할 수 있다.
- GoF 디자인 패턴(Gangs of Four)

- Member
```js
package day19;


public class Member {
		//이름, 아이디, 마일리지
		//final 필드의 초기값은 선언할 때, 또는 생성자에서
	    //final 필드가 초기화가 안 되면 에러 발생 	
		final String memId;
		String memName;
		int memMileage;
		
		static int memberCount ; // 회원수 : 공용적으로 사용할 변수
		
		public Member(String memId, String memName) {
			this.memId = memId ;
			this.memName = memName;
			this.memberCount++;
		}
		
		public String info() {
			String r = String.format(
					"아이디 : %s\n성명 : %s\n마일리지 : %d\n회원수 : %d\n",
					memId, memName, memMileage, memberCount);
			return r;
			
		}
		
}
```
- MemberService

```js
package day19;

public class MemberService {
		//고정적으로 회원 5명을 배열에 담아놓고
		//회원검색 메서드
	private static Member[] members = null;
	
	static {
		members = new Member[5] ;
		members[0] = new Member("malja" , "김말자");
		members[1] = new Member("nolja" , "야놀자");
		members[2] = new Member("haja" , "공부하자");
		members[3] = new Member("gayoung" , "가영엄마");
		members[4] = new Member("misun" , "지각미선");
	}
	
		public Member findMember(String id) {
			//Member[] Member = members;
			Member m = null;
			int len = members.length ;
			for(int i = 0 ; i < len; i++) {
				if(members[i].memId.equals(id)) { //문자열(String) 비교는 .equals()로
					m = members[i];
					return m;
				}
			}	
					return m;
				}
			//찾으면 해당 객체 리턴
			//없으면 널을 리턴
	
	//정적 클래스 변수(통상 변수이름은 instance)
	private static MemberService instance = new MemberService();
	
	//생성자를 감추어야된다.(Private)
	private MemberService() {
		
	}
	
	//해당 정적변수를 리턴하는 메서드 생성 getInstance()

		
		public static MemberService getInstance() {
		if(instance == null) instance = new MemberService();
		return instance;
	}
		//두 숫자를 받아서 합을 구해 리턴하는 메서드
		public int sum(int x, int y) {
			int s = x + y;
			return x + y ;
		}
		
		public Member createMember(String id, String name) {
			Member m = new Member(id, name);
			return m;
		}
		//멤버서비스를 리턴하는 메서드 생성
		public MemberService createMemberService() {
		MemberService s = new MemberService() ;
		return s ;
	}
	
}
```
- MemberServiceTest
 ```js
package day19;

public class MemberServiceTest {

	public static void main(String[] args) {
		MemberService ms1 = MemberService.getInstance();
		MemberService ms2 = MemberService.getInstance();
		MemberService ms3 = MemberService.getInstance();
		
		System.out.println(ms1);
		System.out.println(ms2);
		System.out.println(ms3);
		
		Member m = ms1.findMember(new String("haja"));
			if(m !=null) {
				System.out.println(m.info());
			}else {
				System.out.println("해당 회원이 존재하지 않습니다.");
			}
			//final 필드는 변경 불가
			//final 메서드는 오버라이드가 불가능
			//memId
		}
	}
```

### 6.7.4 생성자 오버로딩
- 생성자 오버로딩이란 매개 변수를 달리하는 생성자를 여러 개 선언하는 것을 말한다.
- 매개 변수의 타입, 개수, 순서가 다르게 선언
- 생성자 오버로딩 시 주의할 점은 매개 변수의 타입과 개수 그리고 선언된 순서가 똑같을 경우 매개 변수이름만 바꾸는 것은 생성자 오버로딩이라고 볼 수 없다.
- 잘못된 생성자 오버로딩
```js
Car(String model, String color)
Car(String color, String model) // 오버로딩이 아님
```


## 6.8 메소드
- 메소드는 객체의 동작에 해당하는 중괄호 블록{}을 말한다.
- 메소드는 필드를 읽고 수정하는 역할도 하지만, 다른 객체를 생성해서 다양한 기능을 수행하기도 한다.
- 메소드는 객체 간의 데이터 전달의 수단으로 사용된다.
- 외부로부터 매개값을 받을 수 있고, 실행 후 어떤 값을 리턴할 수도 있다.

### 6.8.1 메소드 선언
- 메소드 선언은 선언부(리턴타입, 메소드이름, 매개변수선언)와 실행 블록으로 구성된다.

### 6.8.2 리턴문
- 리턴값이 있는 메소드 : 메소드 선언에 리턴 타입이 있는 메소드는 반드시 리턴문을 사용해서 리턴값을 지정해야 한다. 만약 return문이 없다면 컴파일 오류가 발생한다. return문이 실행되면 메소드는 즉시 종료된다.
- 리턴값이 없는 메소드(void) : void로 선언된 리턴값이 없는 메소드에서도 return문을 사용할 수 있다.
  
### 6.8.3 메소드 호출
- 메소드는 클래스 내외부의 호출에 의해 실행된다. 클래스 내부의 다른 메소드에서 호출할 경우에는 단순한 메소드 이름으로 호출하면 되지만, 클래스 외부에서 호출할 경우에는 우슨 클래스로부터 객체를 생성한 뒤, 참조 변수를 이용해서 메소드를 호출해야 한다.

### 6.8.4 메소드 오버로딩
- 클래스 내에 같은 이름의 메소드를 여러 개 선언하는 것을 메소드 오버로딩이라고 한다. 오버로딩의 사전적 의미는 많이 싣는 것을 뜻한다. 하나의 메소드 이름으로 여러 기능을 담는 다 하여 붙여진 이름이다.

## 6.10 정적 멤버와 static
- 정적은 고정된이란 의미를 가지고 있다. 정적 멤버는 클래스에 고정된 멤버로서 객체를 생성하지 않고 사용할 수 있는 필드와 메소드를 말한다. 이들을 각각 정적필드, 정적 메소드라고 부른다. 정적 멤버는 객체에 소속된 멤버가 아니라 클래스에 소속된 멤버이기 때문에 클래스 멤버라고 한다.
- 공용으로 사용할 것들을 스태틱으로 만들면 좋다.

### 6.10.1 정적 멤버 선언
- 필드를 선언할 때 인스턴스 필드로 선언할 것인가, 아니면 정적 필드로 선언할 것인가의 판단 기준은 객체마다 가지고 있어야 할 데이터라면 인스턴스 필드로 선언하고, 객체마다 가지고 있을 필요성이 없는 공용적인 데이터라면 정적 필드로 선언하는 것이 좋다.
- 예를 들어 Calculator 클래스에서 원의 넓이나 둘레를 구할 때 필요한 파이는 Calculator 객체마다 가지고 있을 필요가 없는 변하지 않는 공용적인 데이터이므로 정적 필드로 선언하는 것이 좋다.

### 6.10.3 정적 초기화 블록
- 정적 필드는 객체 생성 없이도 사용해야 하므로 생성자에서 초기화 작업을 할 수 없다.
- 정적 블록은 클래스가 메모리로 로딩될 때 자동적으로 실행된다. 정적 블록은 클래스 내부에 여러 개가 선언되어도 상관없다. 클래스가 메모리로 로딩될 때 자동적으로 실행된다. 정적 블록은 클래스 내부에 여러 개가 선언되어도 상관없다. 클래스가 메모리로 로딩될 때 선언된 순서대로 실행된다.

### 6.10.5 싱글톤
- 가끔 전체 프로그램에서 단 하나의 객체만 만들도록 보장해야 하는 경우가 있다. 단 하나만 생성된다고 해서 이 객체를 싱글톤이라고 한다. 싱글톤을 만들려면 클래스 외부에서 new 연산자로 생성자를 호출할 수 없도록 막아야 한다. 생성자를 호출한 만큼 객체가 생성되기 때문이다. 생성자를 외부에서 호출할 수 없도록 하려면 생성자 앞에 private 접근 제한자를 붙여주면 된다. 외부에서 생성자 호출을 막기 위해 private를 붙여준다는 것만 알아두자

## 6.11 final 필드와 상수
### 6.11.1 final 필드
- 생성자는 final 필드의 최종 초기화를 마쳐야 하는데, 만약 초기화되지 않은 final 필드를 그대로 남겨두면 컴파일 에러가 발생한다.
- 예를 들어 주민등록번호 필드는 한 번 값이 저장되면 변경할 수 없도록 final 필드로 선언했다. 하지만 주민등록번호는 person 객체가 생성될 때 부여되므로 Person 클래스 설계시 초기값을 미리줄 수 없다. 그래서 생성자 매개값으로 주민등록번호를 받아서 초기값으로 지정해주었다.

###6.11.2 상수(static final)
- 일반적으로 불변의 값을 상수라고 부른다. 불변의 값은 수학에서 사용되는 원주율 파이나, 지구의 무게 및 둘레 등이 해당된다. 이런 불변의 값을 저장하는 필드를 상수라고 한다. 상수는 static이면서 final이어야 한다. Static final 필드는 객체마다 저장되지 않고, 클래스에만 포함된다. 그리고 한 번 초기값이 저장되면 변경할 수 없다.

## 6.12 패키지
- 클래스를 체계적으로 관리하지 않으면 클래스 간의 관계가 뒤엉켜 복잡하고 난해한 프로그램이 되어 결국 유지보수가 어렵게 된다.
- 패키지는 단순히 파일 시스템의 폴더 기능만 하는 것이 아니라 클래스의 일부분이다. 패키지는 클래스를 유일하게 만들어주는 식별자 역할을 한다. 클래스 이름이 동일하더라도 패키지가 다르면 다른 클래스로 인식한다.
## 6. 13 접근 제한자
-  접근 제한자는 public, protected, default, private와 같이 네 가지 종류가 있다. Public 접근 제한자는 단어 뜻대로 공개한다는 의미를 가지고 있다. 또한 외부 클래스가 자유롭게 사용할 수 있는 공개 멤버를 만든다. Protected 접근 제한자는 패키지 또는 자식 클래스에서 사용할 수 있는 멤버를 만든다. 위 세가지 접근 제한자가 적용되지 않는 멤버는 default 접근 제한을 가진다. Default 접근 제한자는 같은 패키지에 소속된 클래스에서만 사용할 수 있는 멤버를 만든다.  


- 계좌 정보
```js
package day20;


public class Account {
	private String ano;		//계좌번호(읽기 가능, 쓰기 금지)
	private String owner;	//소유자(읽기 가능, 쓰기 가능)
	private  int balance ;	//잔고(읽기 가능, 쓰기 금지)
	
	
	public String getOwner() {
		return owner;
	}


	public void setOwner(String owner) {
		this.owner = owner;
	}


	public String getAno() {
		return ano;
	}


	public int getBalance() {
		return balance;
	}


	//생성자(계좌번호, 소유자) : 잔고 0
	//생성자(계좌번호, 소유자, 잔고)
	public Account(String ano, String owner) {
		this(ano, owner, 0);
//		this.ano = ano;
//		this.owner = owner;
//		this.balance = 0;
	
	}
	
	public Account(String ano, String owner, int balance) {
		this.ano = ano;
		this.owner = owner;
		this.balance = balance;
	}


	//입금 : deposit
	public void deposit(int amount) {
		//입금한 금액을 잔고에 추가
		//balance = balance +  amount ;
		balance += amount;
	}

	//촐금 : withdraw()
	public int withdraw(int amount) {
	
		   //잔고가 있다면 amount 만큼 출금, 잔고 정리
		   //잔고가 부족하다면 메시지출력, 0리턴
		if(balance < amount) {
			System.out.println("잔고가 부족합니다.");
			return 0;	//결과를 리턴하면서 빠져나간다.
		}
		balance -= amount;
		return amount;	
	}
	}

```
- 계좌 정보
```js
package day20;

public class AccountTest {

	//계좌정보를 보여주는 메서드(정적X)
	public void accountInfo(Account ac) {
		System.out.println("-----[계좌정보]-----");
		System.out.println("계좌번호 : " + ac.getAno());
		System.out.println("소 유 자 : " + ac.getOwner());
		System.out.println("잔    고 : " + ac.getBalance());
		
	}
	
	
	public static void main(String[] args) {
		Account malja = new Account("2021 - 0001", "김말자", 1000000);
		Account sunja = new Account("2021 - 0002", "이순자", 500000);
		System.out.println("---------------");

		malja.deposit(3500);
		//말자의 계좌정보를 보여주세요
		malja.deposit(15000);
		//말자의 계좌정보를 보여주세요
		
		AccountTest at = new AccountTest();
		at.accountInfo(malja);
		
		int amt = sunja.withdraw(60000);
		at.accountInfo(sunja);
		System.out.println("순자 출금액 : " + amt);
		sunja.withdraw(35000);
		//순자의 계좌정보를 보여주세요
	}
}
```

## 6.15 어노테이션
- 어노테이션은 메타데이터라고 볼 수 있다. 메타데이터란 다른 데이터를 설명해주는 데이터다 .
- 어노테이션의 용도
1. 컴파일러에게 코드 문법 에러를 체크하도록 정보를 제공
2. 소프트웨어 개발 툴이 빌드나 배치시 코드를 자동으로 생성할 수 있도록 정보를 제공
3.실행시 런타임 시 특정 기능을 실행하도록 정보를 제공

### 6.15.1 어노테이션 타입 정의와 적용
- @interface를 사용해서 어노테이션을 정의하며, 그 뒤에 사용할 어노테이션 이름이 온다.
```js
public @interface AnnotationName
```
- 어노테이션은 엘리먼트를 멤버로 가질 수 있다. 각 엘리먼트는 타입과 이름을 구성되며, 디폴트 값을 가질 수 있다.
```js
public @interface AnnotationName {
	타입 elementName() [default 값]; //엘리먼트 선언
}
```
- 엘리먼트 타입으로는 int나 double과 같은 기본 데이터 타입이나 String, 열거 타입, Class 타입, 그리고 이들의 배열 타입을 사용할 수 있다.

```js
Public @interface AnnotationName{
	String value();			//기본 엘리먼트 선언
	int elementName() defualt 5;
}
```

### 6.15.3 어노테이션 유지 정책
- 어노테이션 정의 시 한 가지 더 추가해야 할 사항은 용도에 따라 소스상에만 유지할 건지, 컴파일된 클래스까지 유지할 건지, 런타임 시에도 유지할 건지를 지정해야 한다.
- 리플렉션이란 런타임 시에 클래스의 베타 정보를 얻는 기능을 말한다.  예를 들어 클래스가 가지고 있는 필드가 무엇인지, 어떤 생성자를 갖고 있는지, 어떤 메소드를 가지고 있는지, 적용된 어노테이션이 무엇인지 알아내는 것이 리플렉션이다. 리플렉션을 이용해서 런타임 시에 어노테이션 정보를 얻으려면 어노테이션 유지 정책을 RUNTIME으로 설정해야 한다.


### 6.15.4 런타임 시 어노테이션 정보 사용하기
- 런타임 시에 어노테이션이 적용되었는지 확인하고 엘리먼트 값을 이용해서 특정 작업을 수행하는 방법
- 어노테이션 자체는 아무런 동작을 가지지 않는 단지 표식일 뿐이지만, 리플렉션을 이용해서 어노테이션의 적용 여부와 엘리먼트 값을 읽고 적절히 처리할 수 있다. 클래스에 적용된 어노테이션 정보를 얻으려면 java.lang.class를 이용하면 되지만,  필드, 생성자, 메소드에 적용된 어노테이션 정보를 얻으려면 Class의 다음 메소드를 통해서 java.lang.reflect 패키지의 Field, Constructor, Method 타입의 배열을 얻어야 한다.

- 리턴 타입 : Field[] / 메소드명(매개 변수) : getFields() / 설명 : 필드 정보를 Field 배열로 리턴
- 리턴 타입 : Constructor[] / 메소드명(매개 변수) : getConstructors() / 설명 : 생성자 정보를 Constructor 배열로 리턴
- 리턴 타입 : Method[] / 메소드명(매개 변수) : getDeclaredMethods() / 설명 : 메소드 정보를 Method 배열로 리턴

## Chapter 07 상속
### 7.1 상속 개념
- 객체 지향 프로그램에서도 부모 클래스의 멤버를 자식 클래스에게 물려줄 수 있다.
- 상속은 이미 잘 개발된 클래스를 재사용해서 새로운 클래스를 만들기 때문에 코드의 중복을 줄여준다.
- 부모 클래스
```js
public class A {
	int field1;
	void method1() {...}
}
```
- 자식 클래스
```js
public class B extends A {
	String field2;
	void method2() {...}
}
```

- 상속을 해도 부모 클래스의 모든 필드와 메소드를 물려받는 것은 아니다. 부모 클래스에서 private 접근 제한을 갖는 필드와 메소드는 상속 대상에서 제외된다.

### 7.2 클래스 상속
- 현실에서 상속은 부모가 자식을 선택해서 물려주지만, 프로그램에서는 자식이 부모를 선택한다. 자식 클래스를 선언할 때 어떤 부모 클래스를 상속받을 것인지를 결정하고 선택된 부모 클래스는 다음과 같이 extends 뒤에 기술한다.
```js
class 자식클래스 extends 부모클래스 {
	//필드
	//생성자
	//메소드
}
```
- 다른 언어와는 달리 잦바는 다중 상속을 허용하지 않는다. 즉 여러 개의 부모 클래스를 상속할 수 없다. 그러므로 다음과 같이 extends 뒤에는 단 하나의 부모 클래스만 와야 한다.

### 7.3 부모 생성자 호출
- super()는 부모의 기본 생성자를 호출한다.
- 만약 직접 자식 생성자를 선언하고 명시적으로 부모 생성자를 호출하고 싶다면
```js
자식클래스(매개변수선언, …) {
	super(매개값, …);
	...
}
```
- super(매개값, ...)는 매개값의 타입과 일치하는 부모 생성자를 호출한다. 만약 매개값이 타입과 일치하는 부모 생성자가 없을 경우 컴파일 오류가 발생한다.
- super(매개값, ...)는 반드시 자식 생성자 첫 줄에 위치해야 한다.
#### 계좌 카드, 마이너스 통장, 보너스카드 만들기
- Account
```js
package day22;


public class Account {
	protected String ano;		//계좌번호(읽기 가능, 쓰기 금지)
	protected String owner;	//소유자(읽기 가능, 쓰기 가능)
	protected int balance ;	//잔고(읽기 가능, 쓰기 금지)
	//접근제한자 미선언시 기본 dafault : 하위패키지도 안됩니다.

	
	public Account(String ano, String owner) {
		this(ano, owner, 0);
	}
	
	public Account(String ano, String owner, int balance) {
		this.ano = ano;
		this.owner = owner;
		this.balance = balance;
	}
	
	public String getOwner() {
		return owner;
	}


	public void setOwner(String owner) {
		this.owner = owner;
	}


	public String getAno() {
		return ano;
	}


	public int getBalance() {
		return balance;
	}

	
	public void deposit(int amount) {
		balance = amount + balance;
	}

	public int withdraw(int amount) {
		if (amount > balance) {
			System.out.println("잔고가 부족합니다.");
			return 0;
		}
		
		balance -= amount;
		return amount;
		
	}
	
	public void accountInfo() {
		System.out.println("--------[계좌정보]--------");
		System.out.println("계좌정보 : " + this.getAno());
		System.out.println("소 유 자 : " + this.getOwner());
		System.out.println("잔   고 : " + String.format("%d", this.getBalance()));
		
	}
	}
```
- BonusCard
```js
package day22;

public class BonusCard {
	
	private String ano;		//계좌번호(읽기 가능, 쓰기 금지)
	private String owner;	//소유자(읽기 가능, 쓰기 가능)
	private  int balance ;	//잔고(읽기 가능, 쓰기 금지)
	private int point;

	
	public BonusCard(String ano, String owner, int balance, int point) {
		super();
		this.ano = ano;
		this.owner = owner;
		this.balance = balance;
		this.point = point;
	}
	
	public int getPoint() {
		return point;
	}

	public String getOwner() {
		return owner;
	}

	public void setOwner(String owner) {
		this.owner = owner;
	}

	public String getAno() {
		return ano;
	}

	public int getBalance() {
		return balance;
	}

	public int getcreditLimit() {
		return balance;
	}
	
	public void deposit(int amount) {
		balance = amount + balance;
		point = (int)(amount * 0.01);
	}

	public int withdraw(int amount) {
		if (amount > balance + point) {
			System.out.println("잔고가 부족합니다.");
			return 0;
		}
		
		balance = balance + point - amount;
		return amount;
	}
	
	public void accountInfo() {
		System.out.println("--------[계좌정보]--------");
		System.out.println("계좌정보 : " + this.getAno());
		System.out.println("소 유 자 : " + this.getOwner());
		System.out.println("잔   고 : " + String.format("%d", this.getBalance()));
		System.out.println("포인트 : " + this.getPoint());
		System.out.println();
	
	}
	}
```
- CardTest
```sql
package day22;

public class CardTest {

	public static void main(String[] args) {
		CheckCard checkCard = new CheckCard("2021-0001", "주헌아빠", 100000, "0000-0000-0001");
		checkCard.deposit(3000);
		checkCard.withdraw(75000);
		checkCard.accoutInfo();
		
		boolean res = checkCard.pay("0000-0000-0001", 15000);
		if(res) {
			System.out.println("카드결제 성공");
		}else {
	     	System.out.println("카드결제 실패");
	    }
	 	checkCard.accoutInfo();
	 	
	 	BonusCard bonusCard = new BonusCard("2021-0002", "호준아빠", 5000, 0);
	 	bonusCard.deposit(10000);
	 	bonusCard.accountInfo();
	 	bonusCard.withdraw(15050);
	
	 	MinusAccount minusAccount = new MinusAccount("2021-0003", "태정", 5000);
	 	minusAccount.deposit(3000);
	 	minusAccount.accountInfo();
	 	minusAccount.withdraw(10000);
	 	minusAccount.accountInfo();
}
}
```
- CheckCard
```js
package day22;

public class CardTest {

	public static void main(String[] args) {
		CheckCard checkCard = new CheckCard("2021-0001", "주헌아빠", 100000, "0000-0000-0001");
		checkCard.deposit(3000);
		checkCard.withdraw(75000);
		checkCard.accoutInfo();
		
		boolean res = checkCard.pay("0000-0000-0001", 15000);
		if(res) {
			System.out.println("카드결제 성공");
		}else {
	     	System.out.println("카드결제 실패");
	    }
	 	checkCard.accoutInfo();
	 	
	 	BonusCard bonusCard = new BonusCard("2021-0002", "호준아빠", 5000, 0);
	 	bonusCard.deposit(10000);
	 	bonusCard.accountInfo();
	 	bonusCard.withdraw(15050);
	
	 	MinusAccount minusAccount = new MinusAccount("2021-0003", "태정", 5000);
	 	minusAccount.deposit(3000);
	 	minusAccount.accountInfo();
	 	minusAccount.withdraw(10000);
	 	minusAccount.accountInfo();
}
}
```
- InheritanceTest
```js
package day22;

public class CardTest {

	public static void main(String[] args) {
		CheckCard checkCard = new CheckCard("2021-0001", "주헌아빠", 100000, "0000-0000-0001");
		checkCard.deposit(3000);
		checkCard.withdraw(75000);
		checkCard.accoutInfo();
		
		boolean res = checkCard.pay("0000-0000-0001", 15000);
		if(res) {
			System.out.println("카드결제 성공");
		}else {
	     	System.out.println("카드결제 실패");
	    }
	 	checkCard.accoutInfo();
	 	
	 	BonusCard bonusCard = new BonusCard("2021-0002", "호준아빠", 5000, 0);
	 	bonusCard.deposit(10000);
	 	bonusCard.accountInfo();
	 	bonusCard.withdraw(15050);
	
	 	MinusAccount minusAccount = new MinusAccount("2021-0003", "태정", 5000);
	 	minusAccount.deposit(3000);
	 	minusAccount.accountInfo();
	 	minusAccount.withdraw(10000);
	 	minusAccount.accountInfo();
}
}
```

- MinusAccount
```js
package day22;

public class MinusAccount extends Account {
	
	private int creditLimit;

	public MinusAccount(String ano, String owner, int creditLimit) {
		super(ano, owner); // 부모생성자 호출, super(), 첫라인\
		//super(ano, owner)
	}
	
	@Override//부모의 메서드를 재정의 한다. 체크해주세요
	public int withdraw(int amount) {
		if((balance + creditLimit) < amount) {
			System.out.println("잔고가 부족합니다.");
			return 0;
		}
		balance -= amount;
		return amount;
	}
	//accountInfo를 재정의해서 기존내용 + "신용한도 : 20,000"
	
	public void accountInfo() {
		super.accountInfo();
//		System.out.println("--------[계좌정보]--------");
//		System.out.println("계좌정보 : " + this.getAno());
//		System.out.println("소 유 자 : " + this.getOwner());
//		System.out.println("잔   고 : " + String.format("%d", this.getBalance()));
		System.out.println("신용한도 : " + String.format("%d", creditLimit));
		
	}
	
}
```

### 7.7 타입 변환과 다형성
#### 7.7.1 자동 타입 변환
- 자동 타입 변환은 프로그램 실행 도중에 자동적으로 타입 변환이 일어하는 것을 말한다. 자동 타입 변환은 다음과 같은 조건에서 일어난다.
```js
 	자동 타입 변환
부모클래스 변수 = 자식클래스타입;
```
- 부모 타입으로 자동 타입 변환된 이후에는 부모 클래스에 선언된 필드와 메소드만 접근이 가능하다. 비록 변수는 자식 객체를 참조하지만 변수로 접근 가능한 멤버는 부모 클래스 멤버로만 한정된다. 그러나 예외가 있는데, 메소드가 자식 클래스에서 오버라이딩 되었다면 자식 클래스의 메소드가 대신 호출된다. 이것은 다형성과 관련이 있기 때문에 매우 중요한 성질이다.

#### 7.7.5 강제 타입 변환(Casting)
- 강제 타입 변환(Casting)은 부모 타입을 자식 타입으로 변환하는 것을 말한다.
#### 7.7.6 객체 타입 확인(instanceof)
- 어떤 객체가 어떤 클래스의 인스턴스인지 확인하려면 instanceof 연산자를 사용할 수 있다.
- instanceof 연산자의 좌항은 객체가 오고, 우항은 타입이 오는데, 좌항의 객체가 우항의 인스턴스이면 즉 우항의 타입으로 객체가 생성되었다면 true를 산출하고 그렇지 않으면 false를 산출한다.
```js
boolean result = 좌항(객체) instanceof 우항(타입)
```


```js
package day23;

import day22.Account;
import day22.MinusAccount;
import day22.card.CheckCard;

public class PolymorphismTest {
	// 부모 타입 변수 = new 자식타입 <- 자동타입변환
	public static void main(String[] args) {
		
		Account acc = new CheckCard("2021-0004" , "사승원", 0 ,"0000-1111-2222") ;
		acc.deposit(5000);
		acc.deposit(3200);
		acc.accountInfo();	// 실 객체의 메서드 호출 (오버라이드 된 경우)
//		acc.pay("0000-1111-2222", 3000);
//		acc.accountInfo();
		
		//형변환을 통해서 해당 메서드 호출 가능
		CheckCard cc = (CheckCard)acc;
		cc.pay("0000-1111-2222", 1200);
		acc.accountInfo();
		
		Account acc2 = new MinusAccount("2021-0005", "사승1", 0);
		acc2.deposit(5000);
		acc2.deposit(3200);
		acc2.accountInfo();
		// 실제랑 다르게 형 변환, instanceof 연산자를 통해서 확인. "객체 instanceof 타입"  
		if(acc2 instanceof CheckCard) {
			CheckCard cc2 = (CheckCard)acc2;
			cc.pay("0000-1111-2222", 1200);
			acc.accountInfo();
		}else {
			System.out.println("현재 " + acc2.getOwner() + "님의 계정은 체크카드가 아닙니다.(Minus카드)");
		}
		
	}
}
```
```js
package day23;

import day22.Account;
import day22.MinusAccount;
import day22.card.CheckCard;

public class PolymorphismTest2 {
	public static void main(String[] args) {
		CheckCard cc1 = new CheckCard("2021-0001" , "사승2", 200 ,"0000-1111-2222") ;
		CheckCard cc2 = new CheckCard("2021-0002" , "사승3", 1500 ,"0000-1111-2222") ;
		CheckCard cc3 = new CheckCard("2021-0003" , "사승4", 500 ,"0000-1111-2222") ;
		MinusAccount ma1 = new MinusAccount("2021-0004" , "사승5", 300, 3000);
		MinusAccount ma2 = new MinusAccount("2021-0005" , "사승6", 0, 5000);

		CheckCard cc4 = new CheckCard("2021-0003" , "사승7", 500 ,"0000-1111-2222") ;
		CheckCard cc5 = new CheckCard("2021-0003" , "사승8", 500 ,"0000-1111-2222") ;
		MinusAccount ma3 = new MinusAccount("2021-0005" , "사승9", 0, 5000);
		
//		CheckCard[] cards = {cc1, cc2, cc3, cc4, cc5};
//		MinusAccount minuses = {ma1, ma2, ma3};
		Account[] accounts = {cc1, cc2, cc3, cc4, cc5, ma1, ma2, ma3};
		for (int i = 0; i < accounts.length; i++) {
			supportFund(accounts[i]);
			accounts[i].accountInfo();
		}
		
		
//		for(Account acc : acc) {
//		supportFund(cc1);
//		cc1.accountInfo();
	
		
		supportFund(cc1);
		cc1.accountInfo();
		supportFund(cc2);
		cc2.accountInfo();
		supportFund(cc3);
		cc3.accountInfo();
		
		supportFund(ma1);
		ma1.accountInfo();
		supportFund(ma2);
		ma2.accountInfo();
		
		
		
		// 재난지원금 전국민 지원(체크카드는 3000, 마이너스통장 5000)
		
	}
	public static void supportFund(Account check) {
		if(check instanceof CheckCard){
			check.deposit(3000);
		}else if(check instanceof MinusAccount)
			check.deposit(5000);

		
	}
	
}
```


### 7.8 추상 클래스
####7.8.1 추상 클래스의 개념
- 클래스에서도 추상 클래스가 존재한다. 객체를 직접 생성할 수 있는 클래스를 실체 클래스라고 한다면 이 클래스들의 공통적인 특성을 추출해서 선언한 클래스를 추상 클래스라고 한다. 추상 클래스와 실체 클래스는 상속의 관계를 가지고 있다. 추상 클래스가 부모이고 실체 클래스가 자식으로 구현되어 실체 클래스는 추상 클래스의 모든 특성을 물려받고,  추가적인 특성을 가질 수 있다.
- 추상 클래스는 실체 클래스의 공통되는 필드와 메소드를 추출해서 만들었기 때문에 객체를 직접 생성해서 사용할 수 없다. 다시 말해서 추상 클래스는 new 연산자를 사용해서 인스턴스를 생성시키지 못한다.

#### 7.8.2 추상 클래스의 용도
- 실체 클래스들의 공통된 필드와 메소드의 이름을 통일한 목적
-- 실체 클래스를 설계하는 사람이 여러 사람일 경우, 실체 클래스마다 필드와 메소드가 제각기 다른 이름을 가질 수 있다. 예를 들어 소유자의 이름을 저장하는 필드를 Telephone에서는 owner라고 하고, SmartPhone에서는 user라고 할 수 있다. 그리고 전원을 켜다라는 메소드를 Telephone에서는 turnOn()으로 설계하고, SmartPhone에서는 powerOn()이라고 설계할 수 있다. 동일한 데이터와 기능임에도 불구하고 이름이 다르다 보니, 객체마다 사용 방법이 달라진다. 이것보다는 Phone이라는 추상 클래스에 소유자인 owner 필드와 turnOn() 메소드를 선언하고, Telephone과 SmartPhone운 Phone을 상속함으로써 필드와 메소드 이름을 통일시킬 수 있다.

#### 7.8.3 추상 클래스 선언
- 추상 클래스를 선언할 때에는 클래스 선언에 abstract 키워드를 붙여야 한다. abstract를 붙이게 되면 new 연산자를 이용해서 객체를 만들지 못하고 상속을 통해 자식 클래스만 만들 수 있다.
```js
public abstract class 클래스 {
		// 필드
		// 생성자
		// 메소드
}
```

 Java
- RemoteControl
```js
package day24;

public interface RemoteControl {
	//인터페이스의 모든 멤버는 public으로 (정의 안 해도 )
	//인터페이스의 모든 필드는 상수입니다.
	public static final int MAX_VOLUME = 10;
	int MIN_VALUE = 0;
	
	//인터페이스의 모든 메서드는 추상메서드 입니다.
	public abstract void turnOn();
	public void turnOff() ;
	void setVolume(int volume);
	void info();
	
	//JDK 8 추가 기능
	public default void setMute(boolean mute) {
		if(mute) {
			System.out.println("현재 무음처리 합니다.");
		} else {
			System.out.println("무음처리를 해제합니다.");
		}
	}
	public static void changeBattery() {
		System.out.println("배터리를 교환합니다");
	}
	}


```
- LGRemoteControl
```js
package day24;

public class LGRemoteControl implements RemoteControl{
	
	String model ;
	int volume ;
	
	public LGRemoteControl(String model) {
		this.model = model;
	}
	
	@Override
	public void turnOn() {
		System.out.println(
				this.getClass().getSimpleName() + "TV를 켭니다.");
	}

	@Override
	public void turnOff() {
		System.out.println(
				this.getClass().getSimpleName() + "TV를 끕니다.");
	}

	@Override
	public void setVolume(int volume) {
		if(volume > RemoteControl.MAX_VOLUME) {
			this.volume = RemoteControl.MAX_VOLUME;
		}else if(volume < RemoteControl.MIN_VALUE) {
			this.volume = RemoteControl.MAX_VOLUME;
		}else {
			this.volume = volume;
		}
		System.out.println("TV 현재 볼륨은 " + this.volume);
	}

	@Override
	public void info() {
		System.out.println("제조사 : LG전자");
		System.out.println("모델명 : " + model);
	}
	
}
```
- SamsungRemoteControl
```js
package day24;

public class SamsungRemoteControl implements RemoteControl{
	
	String model ;
	int volume ;
	
	public SamsungRemoteControl(String model) {
		this.model = model;
	}
	
	@Override
	public void turnOn() {
		System.out.println(
				this.getClass().getSimpleName() + "TV를 켭니다.");
	}

	@Override
	public void turnOff() {
		System.out.println(
				this.getClass().getSimpleName() + "TV를 끕니다.");
	}

	@Override
	public void setVolume(int volume) {
		if(volume > RemoteControl.MAX_VOLUME) {
			this.volume = RemoteControl.MAX_VOLUME;
		}else if(volume < RemoteControl.MIN_VALUE) {
			this.volume = RemoteControl.MAX_VOLUME;
		}else {
			this.volume = volume;
		}
		System.out.println("TV 현재 볼륨은 " + this.volume);
	}
	@Override
	public void info() {
		System.out.println("제조사 : 삼성전자");
		System.out.println("모델명 : " + model);
	}
}

```
- Television
```js
package day24;

public class Television {
	
	private RemoteControl rc ;
	
	public Television(RemoteControl rc) {
		this.rc = rc;
	}
	// 메서드 파라미터는 최대한 부모, 인터페이스로 받도록 노
	public void tvOn() {
		System.out.println("리모트 컨트롤러로 TV 켜요");
		rc.turnOn();
	}
	
	public void tvOff() {
		System.out.println("리모트 컨트롤러로 TV 꺼요");
		rc.turnOff();
	}
	
	public void pause(boolean pause) {
		System.out.println("티비 멈춤" + pause);
		rc.setMute(pause);
	}
	
	
	public void changeRemoteControl(RemoteControl rc) {
		this.rc = rc;
		System.out.println("리모트 컨트롤러를 교체했습니다.");
		
	}
}

```
- InterfaceTest2
```js
package day24;

public class InterfaceTest2 {

	public static void main(String[] args) {
		//LGRemoteControl : LG 부평공장에서 파업으로 삼성 걸로 교체해서 판매..
		RemoteControl lgRc = new SamsungRemoteControl("AKB1004");
		Television tv = new Television(lgRc) ;
		tv.tvOn();
		System.out.println("전화왔다...");
		tv.pause(true);
		System.out.println("전화끊었다...");
		tv.pause(false);
		tv.tvOff();

	}

}

```

### 10.1 예외와 예외 클래스
- 컴퓨터 하드웨어의 오동작 또는 고장으로 인해 응용프로그램 실행 오류가 발생하는 것을 자바에서는 에러라고 한다.
- 자바에서는 에러 이외에 예외(exception)라고 부르는 오류가 있다.  예외란 사용자의 잘못된 조작 또는 개발자의 잘못된 코딩으로 인해 발생하는 프로그램 오류를 말한다. 예외가  발생되면 프로그램은 곧바로 종료된다는 점에서 에러와 동일하다. 그러나 예외는 예외처리를 통해 프로그램을 종료하지 않고 정상 실행 상태가 유지되도록 할 수 있다.

- 예외는 두 가지 종류가 있다.
1. 일반 예외 : 컴파일러 체크 예외라고도 하는데, 자바 소스를 컴파일하는 과정에서 예외 처리 코드가 필요한지 검사하기 때문이다. 만약 예외 처리 코드가 없다면 컴파일 오류가 발생한다.
2. 실행 예외 : 실행 예외는 컴파일하는 과정에서 예외 처리 코드를 검사하지 않는 예외를 말한다.
- 컴파일 시 예외처리를 확인하는 차이일 뿐, 두 가지 예외는 모두 예외 처리가 필요하다. 자바에서는 예외를 클래스로 관리한다. JVM은 프로그램을 실행하는 도중에 예외가 발생하면 해당 예외 클래스로 객체를 생성한다. 그리고 나서 예외 처리 코드에서 예외 객체를 이용할 수 있도록 해준다. 모든 예외 클래스들은 다음과 같이 java.lang.Exception 클래스를 상속받는다.
- 일반 예외와 실행 예외 클래스를 구별하는 방법은 일반 예외는 Exception을 상속 받지만RuntimeException을 상속받지 않는 클래스들이고, 실행 예외는 RuntimeException 을 상속받은 클래스들이다.





### 10.2 실행 예외 (RuntimeException)
- 실행 예외는 자바 컴파일러가 체크를 하지 않기 때문에 오로지 개발자의 경험에 의해서 예외 처리 코드를 삽입해야 한다. 만약 개발자가 실행 예외에 대해 예외 처리 코드를 넣지 않았을 경우, 해당 예외가 발생하면 프로그램은 곧바로 종료된다.
```js
package day25;

public class RuntimeException1 {

	public static void main(String[] args) {
		int[] arr = {34 ,67};
		System.out.println("arr[0]" + arr[0]);
		System.out.println("arr[1]" + arr[1]);
		System.out.println("arr[2]" + arr[2]);

//		arr[0]34
//		arr[1]67
//		Exception in thread "main" java.lang.ArrayIndexOutOfBoundsException: 2
//			at day25.RuntimeException1.main(RuntimeException1.java:9)

		
	}

}
```

#### 10.2.1 NullPointerException
- 자바 프로그램에서 가장 빈번하게 발생하는 실행 예외는 java.lang.NullPointerException일 것이다. 이것은 객체 참조가 없는 상태, 즉 null 값을 갖는 참조 변수로 객체 접근 연산자인 도트를 사용했을 때 발생한다. 객체가 없는 상태에서 객체를 사용하려 했으니 예외가 발생하는 것이다.
```js
package day25;

public class RuntimeException {
	public static void main(String[] args) {
		Student st1 = new Student();
		st1.name = "sa";
		st1.kor = 78;
		System.out.println(st1);
		System.out.println(st1.name + ", " + st1.kor + ", " + st1.eng);
		System.out.println(st1.name + ", len = " + st1.name.length() + "upper = " + st1.name.toUpperCase());
		
//		Student st2 = null;
//		day25.Student@2a139a55
//		sa, 78, 0
//		null
//		Exception in thread "main" java.lang.NullPointerException
//			at day25.RuntimeException.main(RuntimeException.java:13)
		
		Student st2 = new Student();
		System.out.println(st2);
		System.out.println(st2.name + ", " + st2.kor + ", " + st2.eng);
		System.out.println(st2.name + ", len = " + st2.name.length() + "upper = " + st2.name.toUpperCase());
		//null 인데 .length나 .toUpperCase(도) 같은 거 쓰면 에러
		
		System.out.println("정상종료");
	}

}
```

#### 10.2.2 ArrayIndexOutOfBoundsException
- 배열에서 인덱스 범위를 초과하여 사용할 경우 실행 예외인 java.lang.ArrayIndexOutOfBouyndsException이 발생한다. 예를 들어 길이가 3인 int[] arr = new int[3] 배열을 선언했다면, 배열을 지정하기 위해 arr[0] ~ arr[2] 를 사용할 수 있다. 하지만 arr[3] 을 사용하면 인덱스 범위를 초과했기 때문에 ArrayIndexOutOfBoundsException이 발생한다.


```js
package day25;

public class exceptiond103 {

	public static void main(String[] args) {
		int[] arr = {34 ,67};
		
		try {
			System.out.println("arr[0]" + arr[0]);
			System.out.println("arr[1]" + arr[1]);
			System.out.println("arr[2]" + arr[2]);
			System.out.println("쉬어");
		}catch (Exception e) {
			System.out.println("에러발생");
			System.out.println("msg = " + e.getMessage());
			System.out.println("---[예외 trace]---");
			e.printStackTrace();
		}
		System.out.println("정상종료");
		
//		arr[0]34
//		arr[1]67
//		에러발생
//		msg = 2			//배열[2]가 잘못 되었다는
//		---[예외 trace]---
//		정상종료
//		java.lang.ArrayIndexOutOfBoundsException: 2
//			at day25.exceptiond103.main(exceptiond103.java:11)

	}
}
```


#### 10.2.3 NumberFormatException
- 프로그램을 개발하다 보면 문자열로 되어 있는 데이터를 숫자로 변경하는 경우가 자주 발생한다.
- 정적 메소드인 parseXXX() 메소드를 이용하면 문자열을 숫자로 변환할 수 있다. 이 메소드들은 매개값이 문자열이 숫자로 변환될 수 있다면 숫자를 리턴하지만, 숫자로 변환될 수 없는 문자가 포함되어 있다면 java.lang.NumberFormatException을 발생시킨다.

#### 10.2.4 ClassCastException
- 타입 변환은 상위 클래스와 하위 클래스 간에 발생하고 구현 클래스와 인터페이스 간에도 발생한다. 이러한 관계가 아니라면 클래스는 다른 클래스로 타입 변환할 수 없다. 억지로 타입 변환을 시도할 경우 ClassCastException이 발생한다.

### 10.3 예외 처리 코드
- 프로그램에서 예외가 발생했을 경우 프로그램의 갑작스러운 종료를 막고, 정상 실행을 유지할 수 있도록 처리하는 코드를 예외 처리 코드라고 한다. 자바 컴파일러는 소스 파일을 컴파일할 때 일반 예외가 발생할 가능성이 있는 코드를 발견하면 컴파일 오류를 발생시켜 개발자로 하여금 강제적으로 예외 처리 코드를 작성하도록 요구한다. 그러나 실행 예외는 컴파일러가 체크주지 않기 때문에 예외 처리 코드를 작성하도록 요구한다. 그러나 실행 예외는 컴파일러가 체크해주지 않기 때문에 예외 처리 코드를 개발자의 경험을 바탕으로 작성해야 한다.
```js
try {
	예외 발생 가능 코드
} catch(예외클래스 e) {
	예외 처리
} finally {
	항상 실행;
}
```
-  try 블록에는 예외 발생 가능 코드가 위치한다. Try 블록의 코드가 예외 발생 없이 정상 실행되면 catch 블록의 코드는 실행되지 않고 finally 블록의 코드를 실행한다. 만약 try 블록의 코드에서 예외가 발생하면 즉시 실행을 멈추고 catch 블록으로 이동하여 예외 처리 코드를 실행한다. 그리고 finally 블록의 코드를 실행한다. Finally 블록은 옵션으로 생략 가능하다. 예외 발생 여부와 상관없이 항상 실행할 내용이 있을 경우에만 finally 블록을 작성해주면 된다.

```js
package day25;

public class Exception1031 {

	public static void main(String[] args) {
		int[] arr = {34 ,67};
		
		try {
			System.out.println("arr[0]" + arr[0]);
			System.out.println("arr[1]" + arr[1]);
			System.out.println("arr[2]" + arr[2]);
			System.out.println("쉬어");
		}catch (Exception e) {
			System.out.println("에러발생");
			System.out.println("msg = " + e.getMessage());
			System.out.println("---[예외 trace]---");
			e.printStackTrace();
		}finally {
			System.out.println("에러 발생여부 상관없이 출력");
		}
		System.out.println("정상종료");

//		arr[0]34
//		arr[1]67
//		에러발생
//		msg = 2
//		---[예외 trace]---
//		java.lang.ArrayIndexOutOfBoundsException: 2
//			at day25.Exception1031.main(Exception1031.java:11)
//		에러 발생여부 상관없이 출력
//		정상종료

	}

}
```

### 10.4 예외 종류에 따른 처리 코드
#### 10.4.2 catch 순서
- 다중 catch 블록을 작성할 때 주의할 점은 상위 예외 클래스가 하위 예외 클래스보다 아래쪽에 위치해야 한다.

#### 10.4.3 멀티 catch
- 자바 7부터 하나의 catch 블록에서 여러 개의 예외 처리할 수 있도록 멀티 catch 기능을 추가했다. Catch 괄호() 안에 동일하게 처리하고 싶은 예외를 |로 연결하면 된다.



## Chapter11 기본 API 클래스

### 11.1 자바 API 도큐먼트
- 프로그램 개발에 자주 사용되는 클래스 및 인터페이스의 모음을 말한다.

### 11.2 java.lang 과 java.util 패키지
- 자바 애플리케이션을 개발할 때 공통적으로 가장 많이 사용되는 패키지는 java.lang 패키지와 java.util.java.time 패키지 일 것이다.

#### 11.2.1 java.lang 패키지
- java.lang 패키지는 자바 프로그램의 기본적인 클래스를 담고 있는 패키지이다. 그렇기 때문에 java.lang 패키지에  있는 클래스와 인터페이스는 import 없이 사용할 수 있다. 지금까지 사용한 String과 System 클래스도 java.lang 패키지에 포함되어 있기 때문에 import하지 않고 사용했다.
--Object : 자바 클래스의 최상위 클래스로 사용
--System : 출력, 입력할 때 사용
--Class : 클래스를 메모리로 로딩할 때 사용
--String : 문자열을 저장하고 여러 가지 정보를 얻을 때 사용
--StringBuffer, StringBuilder : 문자열을 저장하고 내부 문자열을 조작할 때 사용
--Math : 수학 함수를 이용할 때 사용
--Wrapper(Byte, Short, Character, Integer, Float, Double, Boolean, Long) : 기본 타입의 데이터를 갖는 객체를 만들 때 사용, 문자열을 기본 타입으로 변환할 때 사용

#### 11.2.2 java.util 패키지
-Arrays : 배열을 조작
-Calendar : 운영체제의 날짜와 시간을 얻음
-Date : 날짜와 시간 정보를 저장
-Objects : 객체 비교, 널 여부 등을 조사할 때 사용
-StringTokenizer : 특정 문자로 구분된 문자열을 뽑아낼 때 사용
-Random : 난수를 얻을 때 사용

### 11.3 Object 클래스
- 클래스를 선언할 때 extends 키워드로 다른 클래스를 상속하지 않으면 암시적으로 java.lang.Object 클래스로 상속하게 된다. 따라서 자바의 모든 클래스는 Object 클래스의 자식이거나 자손 클래스다. Object는 자바의 최상위 부모 클래스에 해당한다.

#### 11.3.1 객체 비교(equals())
- 자바에서는 두 객체를 동등 비교할 때 equals()메소드를 흔히 사용한다. equals()메소드는 두 객체를 비교해서 논리적으로 동등하면 true를 리턴하고, 그렇지 않으면 false를 리턴한다.

```sql
package day26;

import java.util.HashMap;
import java.util.Map;

public class Ex02Equals {

	public static void main(String[] args) {
		Member m1 = new Member("milkis", "밀키스", "042-719-8850",0);
		Member m2 = new Member("milkis", "밀키스", "042-719-8850",0);
		Member target = new Member("milkis", "밀키스", "042-719-8850",0);
		
		System.out.println("m1.memName = m2.memName" + (m1.memName == m2.memName));
		System.out.println("m1.memName.equals(m2.memName) =" + (m1.memName.equals(m2.memName)));
		if(m1 == m2) {
			System.out.println("m1과 m2는 다르다");
	} else {
			System.out.println("m1과 m2는 다르다!!");
	}
		
		
	//객체간의 물리적인 주소 비교가 아닌
	//논리적인 비교를 하고 싶다면 equals 메서드를 재정의 하면 된다.
	if(m1.equals(m2)) {
		System.out.println("m1.equals(m2)는 같아요");
	} else {
		System.out.println("m1.equals(m2)는 달라");
	}
	
	if(m1.equals(target)) {
		System.out.println("m1.equals(target)는 같아요");
	} else {
		System.out.println("m1.equals(target)는 달라");
		
		
}	//Hash 계열의 컬렉션(HashSet, HashMap, HashTable)은 동등한지 비교하기 위해
	//equals 보다 먼저 두 객체 간의 HashCode를 비교합니다. 그래서
	//hashcode도 재정의 해야만 올바르게 동등객체인지 인식합니다.
	System.out.println("------------------------");
	System.out.println("m1.hashCode() =" + m1.hashCode());
	System.out.println("m2.hashCode() =" + m2.hashCode());
	HashMap<Member, String> map = new HashMap<Member, String>();
	
	map.put(m1, "어렸을 때 부엌에 라이터를 갖고 놀다 잃어버림");
	String r = map.get(m1);
	System.out.println("m1으로 get = " + r);
	
	String r2 = map.get(m2);
	System.out.println("m2으로 get = " + r2);
}
}
```


#### 11.3.2 객체 해시코드(hashCode())

#### 11.3.3 객체 문자 정보(toString())
-Object 클래스의 toString() 메소드는 객체의 문자 정보를 리턴한다. 객체의 문자 정보란 객체를 문자열로 표현한 값을 말한다. 기본적으로 Object 클래스의 toString() 메소드는 “클래스명@16진수해시코드”로 구성된 문자 정보를 말한다.
```sql
package day26;

public class Ex03ToString {

	public static void main(String[] args) {
		Member m1 = new Member("milkis", "밀키스", "042-719-8850",0);
		Member m2 = new Member("malja", "김말자", "042-719-8851",120);
		System.out.println(m1);					//day26.Member@1fc883a3
		System.out.println(m1.toString());		//day26.Member@1fc883a3
		
		m1.scores[0] = 100;
		m1.scores[1] = 99;
		m1.scores[2] = 77;
		
		
		//조상님은 toString : 클래스명@hashCode로 리턴
		//String 클래스는 toString 재정의해서 갖고있던 값을 리턴
		String str = "Hello World";	
		System.out.println(str);					//Hello World
		System.out.println(str.toString());		//Hello World
		
		//실제 개발시, 업무적으로 운영할 때 예외상황이 발생했을 때 남는건 로그파일이다.
		//예외 트레이스 e.printStackTrace + 객체정보
		//여기서 객체정보가 의미없는 해쉬코드보다는 의미있는 정보가 필요하다.
		//그래서 정보를 담는 vo(DTO, 도메인...) 객체는 toString을 꼭 재정의 해야한다.
		
		
		//java는 기본적으로 CallByReference
		//단, 기본형(int, byte, boolean...)은 CallByValue
		//원객체를 보관하려면 복제를 하세요
		Member mt = m1.getMember();
		memberInfoChange(mt);
		System.out.println("m1 = " + m1);
		Member mt2 = m1;
		memberInfoChange(mt2);
		System.out.println("m1 = " + m1);
	}

	
	public static void memberInfoChange(Member mem){
		mem.memName = mem.memName + "사랑해요";
		mem.memMileage = 1004;
		mem.scores[0] = 25;
		mem.scores[1] = 35;
		mem.scores[2] = 45;
		
		System.out.println("memberInfoChange = " + mem);
	
}
}
```


#### 11.3.4 객체 복제(clone())
- 객체 복제는 원본 객체의 필드값과 동일한 값을 가지는 새로운 객체를 생성하는 것을 말한다. 객체를 복제하는 이유는 원본 객체를 안전하게 보호하기 위해서다 . 복제된 객체의 데이터가 훼손되더라도 원본 객체는 아무런 영향을 받지 않기 때문에 안전하게 데이터를 보호할 수 있게 된다.

#### 11.3.5 객체 소멸자(finalize())
- 참조하지 않는 배열이나 객체는 쓰레기 수집기(Garbage Collector)가 힙 영역에서 자동적으로 소멸시킨다. 쓰레기 수집기는 객체를 소멸하기 직전에 마지막으로 객체의 소멸자(finalize())를 실행시킨다.

- 실행 결과를 보면 순서대로 소멸시키지 않고 무작위로 소멸시키는 것을 볼 수 있다. 그리고 전부 소멸 시키는 것이 아니라 메모리의 상태를 보고 일부만 소멸시킨다.
```sql
package day26;

import java.util.HashMap;

public class Ex04filnalize {
	
	public static void main(String[] args) {
		//11.3.5 객체 소멸자(finalize())
		for (int i = 0; i < 100; i++) {
			Member m1 = new Member("id" + i, "밀키스", "042-719-8850", 0);
			m1 = null; //메모리 제거 대상
			System.gc();

//			id1객체가 소멸될 때 필요한 자원정리 등이 필요하면 재정의
//			id16객체가 소멸될 때 필요한 자원정리 등이 필요하면 재정의
//			id15객체가 소멸될 때 필요한 자원정리 등이 필요하면 재정의
//			id17객체가 소멸될 때 필요한 자원정리 등이 필요하면 재정의
//			id19객체가 소멸될 때 필요한 자원정리 등이 필요하면 재정의
//			id21객체가 소멸될 때 필요한 자원정리 등이 필요하면 재정의 ....
// 실행 결과를 보면 순서대로 소멸시키지 않고, 무작위로 소멸시키는 것을 볼 수 있다.
// 그리고 전부 소멸시키는 것이 아니라 메모리의 상태를 보고 일부만 소멸 시킨다.

		}
	}
	}
```

#### 11.5.3 현재 시각 읽기(currentTimemillis(), nanoTime())
- system 클래스의 currentTimeMillis() 메소드와 nanoTime() 메소드는 컴퓨터의 시계로부터 현재 시간을 읽어서 밀리세컨드 단위와 나노세컨드 단위의 long 값을 리턴한다.

```js
long time =  System.currentTimeMillis();
long time =  System.nanoTime();
```
- 리턴 값은 주로 프로그램의 실행 소요 시간 측정에 사용됨

#### 11.5.4 시스템 프로퍼티 읽기(getProperty())
- 시스템 프로퍼티는 JVM이 시작할 때 자동 설정되는 시스템의 속성값을 말한다.
- 시스템 프로퍼티를 읽어오기 위해서는 System.getProperty() 메소드를 이용하면 된다. 이 메소드는 시스템 프로퍼티의 키 이름을 매개값으로 받고, 해당 키에 대한 값을 문자열로 리턴한다.
```js
String  value = System.getProperty(String key)
```

#### 11.5.5 환경 변수 읽기(getnv())
- 환경 변수는 프로그램 상의 변수가 아니라 운영체제에서 이름과 값으로 관리되는 문자열 정보다. 환경변수는 운영체제가 설치될 때 기본적인 내용이 설정되고, 사용자가 직접 설정하거나 응용 프로그램이 설치될 때 자동적으로 추가 설정되기도 한다.
- 자바 프로그램에서는 환경 변수의 값이 필요한 경우 System.getnv() 메소드를 사용한다. 매개값으로 환경 변수 이름을 주면 값을 리턴한다.


```js
package day27;

import java.util.Map;
import java.util.Properties;
import java.util.Set;

public class Ex06Properties {
	//11.5.4 시스템 프로퍼티 읽기
	public static void main(String[] args) {
		String osName = System.getProperty("os.name");
		String javaHome = System.getProperty("java.home");
		String userHome = System.getProperty("user.home");
		String javaVersion = System.getProperty("java.version");
		System.out.println(osName);
		System.out.println(javaHome);
		System.out.println(userHome);
		System.out.println(javaVersion);
//		Linux
//		/usr/lib/jvm/jdk1.8.0_231/jre
//		/home/pc42-pc
//		1.8.0_231
		
		
		System.out.println("------------전체 목록--------------");
		Properties prop = System.getProperties();
		Set keys = prop.keySet();
		for(Object key : keys) {
			String val = System.getProperty(key.toString());
			System.out.println(key + " : " + val);
//			------------전체 목록--------------
//			java.runtime.name : Java(TM) SE Runtime Environment
//			sun.boot.library.path : /usr/lib/jvm/jdk1.8.0_231/jre/lib/amd64
//			java.vm.version : 25.231-b11
//			java.vm.vendor : Oracle Corporation
//			java.vendor.url : http://java.oracle.com/
//			path.separator : :
//			java.vm.name : Java HotSpot(TM) 64-Bit Server VM
//			file.encoding.pkg : sun.io
//			user.country : KR
//			sun.java.launcher : SUN_STANDARD
//			sun.os.patch.level : unknown
//			java.vm.specification.name : Java Virtual Machine Specification
//			user.dir : /home/pc42-pc/eclipse-workspace/chapter01
//			java.runtime.version : 1.8.0_231-b11
//			java.awt.graphicsenv : sun.awt.X11GraphicsEnvironment
//			java.endorsed.dirs : /usr/lib/jvm/jdk1.8.0_231/jre/lib/endorsed
//			os.arch : amd64
//			java.io.tmpdir : /tmp
//			line.separator :
			//너무 길어서 생략...	
			
			
		}
		//11.5.5 환경 변수 읽기
		System.out.println("-------[ENV]-------");
		String oracleHome = System.getenv("ORACLE HOME");
		System.out.println("ORACLE HOME" + oracleHome);
		
		System.out.println("-------[ENV]-------");
		String path = System.getenv("PATH");
		System.out.println("PATH" + path);
		
		System.out.println("-------[ENV]-------");
		Map<String, String> envMap = System.getenv();
		Set<String> keys1 = envMap.keySet();
		for(String key : keys1) {
			String val = System.getenv(key);
			System.out.println(key + " : " + val);
			
//			-------[ENV]-------
//			ORACLE HOMEnull
//			-------[ENV]-------
//			PATH/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/usr/lib/jvm/jdk1.8.0_231/bin
//			-------[ENV]-------
//			PATH : /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/usr/lib/jvm/jdk1.8.0_231/bin
//			XAUTHORITY : /home/pc42-pc/.Xauthority
//			XMODIFIERS : @im=fcitx
//			XDG_DATA_DIRS : /usr/share/cinnamon:/usr/share/gnome:/home/pc42-pc/.local/share/flatpak/exports/share:/var/lib/flatpak/exports/share:/usr/local/share:/usr/share
//			GDMSESSION : cinnamon
//			GTK_IM_MODULE : fcitx
//			DBUS_SESSION_BUS_ADDRESS : unix:path=/run/user/1000/bus
//			XDG_CURRENT_DESKTOP : X-Cinnamon
//			INSIDE_NEMO_PYTHON :
//			SSH_AGENT_PID : 1701
//			QT4_IM_MODULE : fcitx
//			SESSION_MANAGER : local/pc42pc-B150M-DS3H:@/tmp/.ICE-unix/1628,unix/pc42pc-B150M-DS3H:/tmp/.ICE-unix/1628
//			LOGNAME : pc42-pc
//			PWD : /home/pc42-pc
//			LANGUAGE : ko
			//너무 길어서 생략
		}
		
		
	}

}
```




### 11.6 Class 클래스
```js
package day27;

public class Ex07Class {

	public static void main(String[] args) {
		
		// Class : 필드, 생성자, 메서드 정보 (메타데이터)를 관리하는 객체다.
		// Class를 얻는 2가지 방법
		// Class clz = obj.getClass(); // 객체가 존재하는 경우
		// Class clz = Class.forName(String); // 완전한 이름의 객체를 알고 있을 때
		
		// newInstance() 를 통해 동적객체생성 가능
		
	
	}

}
```


#### 11.6.3  동적 객체 생성(newInstance())
- Class 객체를 이용하면 new 연산자를 사용하지 않아도 동적으로 객체를 생성할 수 있다. 이 방법은 코드 작성 시에 클래스 이름을 결정할 수 없고, 런타임 시에 클래스 이름이 결정되는 경우에 매우 유용하게 사용된다.
- Class.forName() 메소드로 Class 객체를 얻은 다음 newInstance() 메소드를 호출하면 Object 타입의 객체를 얻을 수 있다.

```js
package day27;

import java.io.IOException;
import java.io.InputStream;
import java.io.Reader;
import java.lang.reflect.Method;
import java.util.Properties;

import javax.annotation.Resources;

public class Ex08NewInstance {
	
	public static void main(String[] args) {
		String resource = "/day27/action.properties";
		Properties prop = new Properties();
		String className = null;
		
		try {
			//설정파일에 실제 실행할 클래스명 또는 설정 정보를 읽어서 실행중에 읽어서 처리
			InputStream reader = Ex08NewInstance.class.getResourceAsStream(resource);
			prop.load(reader);
			 className = prop.getProperty("action");
			System.out.println(className);
			 Class clz = Class.forName(className.trim()); //trim : 공백제거
			 System.out.println("---메소드 정보---");
			 Method[] methods = clz.getDeclaredMethods();
			 for(Method met : methods) {
				 System.out.println("메소드 명 : " + met.getName());
			 }
			
			//객체 생성(new)
			 Action action = (Action)clz.newInstance();
			 action.execute();
					
		} catch (ClassNotFoundException e) {
			System.out.println(className + "의 클래스명이 잘못되었습니다.");
		} catch (IOException e) {
			System.out.println("파일 로드하는데 실패했습니다.");
			e.printStackTrace();
		} catch (InstantiationException | IllegalAccessException e) {
			System.out.println("객체 생성중 오류 발생가 발생했습니다.");
			e.printStackTrace();
		}
		
	}
	
}
```

### 11.7 String 클래스
#### 11.7.1 String 생성자
```js
package day27;

public class Ex09String {
	//11.7.1 String 생성
	public static void main(String[] args) {
		byte[] bytes = new byte[10];
		try {
			System.out.println("입력 : ");
			int len = System.in.read(bytes);
			for(byte b : bytes) {
				System.out.print(b+ ", ");
			}
			System.out.println("입력한 길이 : " + len);
			String str = new String(bytes, 0 , len -1); //윈도우에선 -2
			System.out.println("str + " +str);
		}catch (Exception e) {
			System.out.println(e.getMessage());
	}
	}
}
```

#### 11.7.2 String 메소드
- 문자 추출 : charAt()
  - 매개값으로 주어진 인덱스의 문자를 리턴함. 여기서 인덱스란 0에서부터 문자열길이 -1 까지의 번호를 말함
```js
String subject  = “자바 프로그래밍”;
char charValue =  subject.charAt(3);
```

- 바이트 배열로 변환 : getBytes()
  - 네트워크로 문자열을 전송하거나, 문자열을 암호화할 때 문자열을 바이트 배열로 변환한다.
```js
byte[] bytes = “문자열”.getBytes();
byte[] byte s= “문자열”.getBytes(Charset charset);
```

- 문자열 찾기 : indexOf()
  - 매개값으로 주어진 문자열이 시작되는 인덱스를 리턴한다. 만약 주어진 문자열이 포함되어 있지 않으면 -1을 리턴한다.
  - 이때 index 변수에는 3이 저장되는데, “자바 프로그래밍”에서 “프로그래밍” 문자열의 인덱스 위치가 3이기 때문이다.
```js
String subject = “자바프로그래밍”
int index = subjectOf(“프로그래밍”);
```


- 문자열 대치 : replace()
  - 첫 번째 매개값인 문자열을 찾아 두 번째 매개값인 문자열로 대치한 새로운 문자열을 생성하고 리턴한다.
```js
String oldStr = “자바 프로그래밍”;
String newStr = oldStr.replace(“자바”, “JAVA”);
```

- 문자열 잘라내기 : substring()
  - 주어진 인덱스에서 문자열을 추출한다.
```js
String ssn = “880815-1234567”;
String firstNum = ssn.substring(0, 6);	//0부터 6까지 출력
String secondNum = ssn.substring(7);	//7부터 끝까지 출력
```

- 알파벳 대소문자 변경 : toLowerCase() , toUpperCase()
```js
String original = “Java Programming”;
String lowerCase = original.toLowerCase();
String upperCase = original.toUpperCase();
```

- 문자열 앞뒤 공백 잘라내기 : trim()
  - 문자열의 앞뒤 공백을 제거한 새로운 문자열을 생성하고 리턴한다. 하지만 앞뒤 공백만 제거할 뿐 중간 공백은 제거하지 않는다.
```js
String oldStr = “         자바 프로그래밍         ”;
String newStr = oldStr.trim();
```

- 문자열 변환 : valueOf()
  - 기본 타입의 값을 문자열로 변환하는 기능
```js
static String valueOf(boolean b)
static String valueOf(char c)
static String valueOf(int i)
static String valueOf(long l)
static String valueOf(double d)
```  

### 11.8 StringTokenizer 클래스
#### 11.8.1 split() 메소드
```js
String[] result = “문자열”.split(“정규표현식”);
```
- &, 쉼표(,), - 를 제외하고 사람 이름을 뽑아내고 싶을 경우
```js
홍길동&이수홍, 박연수, 김자바 - 최명호
String[] names = text.split(“&|,|-”);
```

#### 11.8.2 StringTokenizer 클래스
- 문자열이 한 종류의 구분자로 연결되어 있을 경우 StringTokenizer 클래스를 사용하면 손쉽게 문자열을 분리해 낼 수 있다. StringTokenizer 객체를 생성할 때 첫 번째 매개값으로 전체 문자열을 주고, 두 번째 매개값으로 구분자를 주면 된다.
  - countTokens() : 꺼내지 않고 남아 있는 토큰의 수
  - hasMoreTokens() : 남아 있는 토큰이 있는지 여부
  - nextToken() : 토큰을 하나씩 꺼내옴
```js
StringTokenizer st = new StringTokenizer(“문자열”, “구분자”);
```
```js
String text = “홍길동/이수홍/박연수”
StringTokenizer st = new StringTokenizer(text, “/”);  
```


```js
package day27;

import java.util.StringTokenizer;

public class Ex11StringMethod {

	public static void main(String[] args) {
		String fileName = "스키장 놀러간";
		
		try {
			//ISO-8859-1 : 서유럽어(라틴어, 컴퓨터 기본 캐릭터)
			//ISO-8859-2 : 동유럽어
			//한글 : KSC-5601, EUC-KR, MS949 ...
			
			//getBytes : 바이트 배열로 변환
			//아래 코딩을 해야 한글명 다운로드가 된다.
			String downloadName = new String(fileName.getBytes("UTF-8"),"ISO-8859-1");
			System.out.println(downloadName);
			
			//charAt : 특정 위치의 문자 리턴
			char ch = fileName.charAt(5);
			System.out.println("ch = " + ch);
			
			//indexOf : 문자열 내에서 주어진 문자열의 위치를 리턴
			//만약 주어진 문자열이 포함되어 있지 않으면 -1을 리턴함
			int pos = fileName.indexOf("놀러간");
			System.out.println("pos = " + pos);
			pos = fileName.indexOf("놀러", 3 ); //3번째 이하부터 검색
			System.out.println("6 after pos = " + pos);
			System.out.println("-----------------");
			
			String badMan = "홍길동, 이수홍, 박연수, 김자비";
			//split을 통해 각각 출력
			String[] names = badMan.split(", ");
			int no = 0;
			for(String name : names) {
				System.out.println(++no + " : " + name);
			}
			System.out.println("-----------------");
			StringTokenizer st = new StringTokenizer(badMan, ", ");
			while(st.hasMoreTokens()) {
				System.out.println("cnt = " + st.countTokens());
				System.out.println("token = " + st.nextToken());
			}
			
//			ì¤í¤ì¥ ëë¬ê°
//			ch = 러
//			pos = 4
//			6 after pos = 4
//			-----------------
//			1 : 홍길동
//			2 : 이수홍
//			3 : 박연수
//			4 : 김자비
//			-----------------
//			cnt = 4
//			token = 홍길동
//			cnt = 3
//			token = 이수홍
//			cnt = 2
//			token = 박연수
//			cnt = 1
//			token = 김자비

		}catch (Exception e) {
			e.printStackTrace();
		}
		}

}
```
- 문제
```js
package day27;

public class Ex11StringExam {

	public static void main(String[] args) {
		String exam = "mem_MEMORIAL_day";
		//문제 : 언더바 형식으로된 문자열을 낙타식으로 변환하기
		//위 문자열 "mem_MEMORIAL_day"를 변환처리하여
		//"MemMemorialDay" 또는 "memMemorialDay"로 나오면 됨
		//mem -> Mem
		//split, toLowerCase, indexOf, charAt, String.join("delim", String[])
		System.out.println("----------------");
		
		String newexam = exam.replace("_", "");
		System.out.println(newexam);
		
		String lowerexam = newexam.toLowerCase();
		System.out.println(lowerexam);
		System.out.println("----------------");
		
		String ssn1 = lowerexam.substring(0,3) ;
		System.out.println(ssn1);
		String ssn2 = lowerexam.substring(3,11) ;
		System.out.println(ssn2);
		String ssn3 = lowerexam.substring(11,14) ;
		System.out.println(ssn3);
		
		System.out.println("----------------");
		
		String com1 = ssn1.replace("mem", "Mem");
		String com2 = ssn2.replace("memorial", "Memorial");
		String com3 = ssn3.replace("day", "Day");
		
		
		System.out.println(com1 + com2 + com3);
		
		
		System.out.println("----------------");
		 String[] strs = {"Mem", "Memorial", "Day"};
		 String r = String.join("", strs);
		 System.out.println(r);

	}

}
```

### 11.9 StringBuffer, StringBuilder 클래스
- 문자열을 결합하는 + 연산자를 많이 사용하면 할수록 그만큼 String 객체의 수가 늘어나기 때문에, 프로그램 성능을 느리게 하는 요인이 된다. 문자열을 변경하는 작업이 많을 경우에는 String 클래스를 사용하는 것보다는 java.lang 패키지의 StringBuffer 또는 StringBuilder 클래스를 사용하는 것이 좋다. 이 두 클래스는 내부 버퍼에 문자열을 저장해두고, 그 안에서 추가, 수정, 삭제 작업을 할 수 있도록 설계되어 있다.
- StringBuffer와 StringBuilder의 사용방법은 동일한데 차이점은 StringBuffer는 멀티 스레드환경에서 사용할 수 있도록 동기화가 적용되어 있어 스레드에 안전하지만, StringBuilder는 단일 스레드 환경에서만 사용하도록 설계되어 있다.

```js
StringBuilder sb = new StringBuilder();
```
- StringBuilder 객체가 생성되었다면 다음 메소드를 통해 작업
```
append()			문자열 끝에 주어진 매개값을 추가
insert()				문자열 중간에 주어진 매개값을 추가
delete()			문자열의 일부분을 삭제
deleteChartAt()	문자열에서 주어진 index의 문자를 삭제
replace()			문자열의 일부분을 다른 문자열로 대치
reverse()			문자열의 순서를 뒤바꿈
setCharAt()			문자열에서 주어진 index의 문자를 다른 문자로 대치
```
- String 과 StringBuffer의 차이(String)
```sql
package day26;


public class Ex05StringBuffer {
	
	public static void main(String[] args) {
		String str = "";
		long startTime = System.currentTimeMillis();//1970/1/1시점으로 현재시간을 알려줌
		for (int i = 0; i < 100000; i++) {
			str += "사랑해요";
			//사랑해요 메모리에 생성
			//사랑해요 사랑해요 메모리에 생성
			//String을 계속 누적하면 메모리 낭비
			//String은 문자열을 담는 객체이지, 누적하거나 연산을 위한 전용 객체가 아니다.
		}
		System.out.println("str.length = " + str.length());
		System.out.println("소요시간 = " + (System.currentTimeMillis() - startTime));
		
//		str.length = 4000
//		소요시간 = 6
		
//		str.length = 400000
//		소요시간 = 14081


		
		
		//문자열을 누적하거나 연산을 위해 전용 객체가 따로 있다.
	}
	}
```
- String 과 StringBuffer의 차이(StringBuilder)
```sql
package day26;


public class Ex0StringBuffer2 {
	
	public static void main(String[] args) {
		//문자열을 누적하거나 연산을 위해 전용 객체가 따로 있다.
		// String에 비해 속도가 빨라서 문자열 연산 작업에는 꼭 StringBuffer, StringBuilder 사용
		StringBuilder sb = new StringBuilder();
		long startTime = System.currentTimeMillis();//1970/1/1시점으로 현재시간을 알려줌
		for (int i = 0; i < 10000000; i++) {
			sb.append("사랑해요");
			
//			sb.length = 400
//			소요시간 = 0

//			sb.length = 40000000
//			소요시간 = 234
		}
		System.out.println("sb.length = " + sb.length());
		System.out.println("소요시간 = " + (System.currentTimeMillis() - startTime));
	
	}
	}
```
- StringBuilder 메소드
```sql
package day26;


public class Ex0StringBuffer3 {
	
	public static void main(String[] args) {
		StringBuffer sb = new StringBuffer("1234");
		System.out.println("sb = " + sb.toString());
		sb.delete(0, sb.length());
		System.out.println("delete = " + sb.toString());
		sb.append("사승원");
		System.out.println("append = " + sb.toString());
		sb.insert(3, " 설날");
		System.out.println("insert = " + sb.toString());
		sb.replace(6, 7, " 사랑해요");
		System.out.println("replace = " + sb.toString());
		
		
//		sb = 1234
//				delete =
//				append = 사승원
//				insert = 사승원 설날
//				replace = 사승원 설날 사랑해요

		
	}
	}
```

```js
package day27;

public class Ex12last {
	public static void main(String[] args) {
	String str = "mem_MEMORIAL_day";
			
		String r = camel(str);
		System.out.println("r = " + r);
	}
	
	public static String camel(String orig) {
		String lo = orig.toLowerCase(); //"mem_memorial_day";
		String[] names = lo.split("_");
		StringBuilder sb = new StringBuilder();
		for(String name : names) { // [mem],[memorial],[day]
			System.out.println(name.substring(0, 1).toUpperCase());
			System.out.println(name.charAt(0)+ "," + (char)(name.charAt(0)-32));
			sb.append((char)(name.charAt(0)-32));
			sb.append(name.substring(1));
		}
		return sb.toString();
		}
		
	}


```

- 카드 식별..
```js
package day28;

public class Ex12StringExam2 {

	public static void main(String[] args) {
		String jumin = "781225-1475125";
		//String card = "4673-0902-5031-8168"; // 벤더는 비자카드
		String card = "5570-4203-9290-3026"; //벤더는 마스터 카드
		
		if(isNotDigit(jumin.replace("-", ""))) {
			System.out.println("숫자로 입력해주세요");
		}else {
			if(isCardVerify(card.replace("-", ""))) {
				System.out.println("올바른 카드입니다");
				System.out.println("벤더는 " + getCardBender(card));
			}else {
				System.out.println("잘못된 카드번호입니다");
			}
		}
	}
	public static boolean isNotDigit(String number) {
		return !isDigit(number);
		
	}
	
	public static boolean isDigit(String number) {
		// 9440254060327949
		for(int i = 0 ; i <number.length(); i++){
			char ch = number.charAt(i);
			if(ch < '0' || ch > 57) { //0~9 사이인지 확인 ascii 48~57 사이
				return false;
				}
			}
		return true ;
	
	}
	//주민번호체크
	public static boolean ssnVerify(String ssn) {
		//마스크 234567892345
		//       7812251475125
		//	14 + 24 + 4 + 10 + 12 + 35 + 8 + 36 + 14 + 15 + 4 = 176
		// 11 - (176 % 11) = 11
		// 위 결과가 마지막 주민번호와 같아야 한다.
		// 위 결과가 10보다 크다고 하면 맨 마지막 숫자만
		
			return false;
			
	}
	//카드번호체크
	public static boolean isCardVerify(String card) {
		// 2121 2121 2121 1254
		// 9412 5895 4521 5689
		// 9 + 4 + 2 + 2 + 1 + 8 + 9 + 5 + 8 + 5 + 4 + 1 + 1 + 6 + 7
		// 10이 넘으면 각 숫자를 더해야됨  ex) 18 -> 1 + 8 = 9
		// 10 - (?? % 10) = a
		// a가 카드 맨 뒷 번호랑 같아야 함
		int sum = 0 ;
		int len = card.length();
		//신용카드는 16글자(일부 15)
		if(!(len == 15 || len == 16)) {
			return false;
		} for(int i = 0; i < (len - 1); i++) {
			char ch = card.charAt(i);
			int r = ch -48 ;
			if((i%2) == 0) { // i = 0, 2, 4, 6..
				r = r*2 ;
				if (r >= 10) {
					r = r - 9 ;
					//"28" = (28/10) + (28 % 10)
					//"18" = 1 + 8 -> 9
				}
			}
			sum = sum + r;
		}
		int veri = 10 - (sum % 10);
		if ((veri%10) == (card.charAt(len-1) - 48)){
			return true;
		}
		return false;
	}
	//
	public static String getCardBender(String card) {
		if(card.startsWith("356")) {
			return "JCB 카드";
		}else if(card.startsWith("36")) {
			return "다이너스 카드";
		}else if(card.startsWith("37")) {
			return "아멕스 카드";
		}else if(card.startsWith("4")) {
			return "비자 카드";
		}else if(card.startsWith("5")) {
			return "마스터 카드";
		}else if(card.startsWith("62")) {
			return "유니온페이 카드";
		}else if(card.startsWith("65")) {
			return "BC Global 카드";
		}else if(card.startsWith("9")) {
			return "국내전용 카드";
		}
		
		return "";
	}
}
```


### 11.10 정규 표현식과 Pattern 클래스
#### 11.10.1 정규표현식 작성 방법
- 기본적인 기호들
```sql
 []		 한 개의 문자			[abc] : abc중 하나의 문자
							[^abc] : a,b,c 이외의 하나의 문자
							[a-zA-Z] :   a-z, A-Z 중 하나의 문자
							[a-zA-Z_0-9] : 한 개의 알파벳 또는 한 개의 숫자
\d 		 한 개의 숫자			[0-9] 와 동일
\s 		 공백
\w 		 한 개의 알파벳 또는 한 개의 숫자	 	[a-zA-Z_0-9] 와 동일
? 		 없음 또는 한 개 			
* 		 없음 또는 한 개 이상
+ 		 한 개 이상
{n} 		 정확히 n개
{n,}		 최소한 n개 (n개 이상)
{n, m}     n개에서부터 m개까지
()		 그룹핑
```
- 경계
```sql
^ 		 시작(맨 처음에 기술)
$		 끝(맨 마지막에 기술)
\b  		 단어경계
```
- 그룹핑
```sql
() 		 묶어주는 역할, 캡처(Replace)
```


```js
package day28;

import java.util.regex.Matcher;
import java.util.regex.Pattern;

public class Ex13RugularExpression {

	public static void main(String[] args) {
		//RugularExpression : 정규표현식
		/*
		경계 ^ : 시작을 의미, 처음에 기술
			 $ : 마지막을 의미, 마지막에 기술
			 \b \B : 단어의 경계(비경계)
		문자 [] : 한 문자의 범위
			[abc] : a|b|c
			[a-c] : a|b|c
			[a-zA-Z_0-9] : 일반문자
			[0-9] : 숫자
			[^a-z] : ^가 있으면 부정 소문자가 아닌 한문자
				   . : 임의 한 문자
	 	반복 ? : 앞의 문자(그룹)가 0번 또는 1번
	 		 + : 앞의 문자(그룹)가 1번 이상
	 		 * : 앞의 문자(그룹)가 0번 이상
	 		{n} : 앞의 문자(그룹) n번
	 		{n,} : 앞의 문자(그룹) n번 이상
	 		{n,m} : 앞의 문자(그룹) n번이상 m번 이하
	 	대체 | : or의 의미
	 	그룹 () : 묶음처리, 캡처링은 replace 할 때 유용
	 	역참조 \n : 앞의 그룹과 동일, \1 은 앞의 첫 번째 그룹과 동일
	 	
	 	POSIX 규약 정규표현식
	 	[a-zA-Z0-9_] : [[:alnum:]]
	 	
	 	펄언어에서 좀 더 간결한 표기법(PCRE)을 많이 사용함
	 	\w, \W : [a-zA-Z0-9_]
 	 	\d, \D : [0-9]
 	 	\s, \S : 공백문자 [ \t\r\n]
 	 	\b, \B : 단어의 경계
		*/
		
		
		String[] loves = {"milkis1004", "sa*(sw", "head coach", "ses", "malja"};
		String pa = "[a-zA-Z0-9_]{5,12}";
		//id는 일반문자로 5글자이상 12글자 이하
	
		
		for (int i = 0; i < loves.length; i++) {
			System.out.println(loves[i] + "");
			if(Pattern.matches(pa, loves[i])) {
				System.out.println("패턴이 맞아요");
			}else {
				System.out.println("패턴이 틀려요");
		}
		}
		String dummy = "Hello 1004 my name 34 your age 42";
		Pattern p = Pattern.compile("[0-9] + ");
		Matcher m = p.matcher(dummy)	;
		int count = 0 ;
		while(m.find()) {
			count++;
			System.out.println("Matcher Number = " + count);
			System.out.println("Group = " + m.group());
			System.out.println("Start = " + m.start());
			System.out.println("End = " + m.end());
		}
		
		String p2 = "([가-힣]{2,4})\\s+(\\d\\d)(\\d\\d)(\\d\\d).+";
		String res = "오성현 921014-1356789".replaceAll(p2, "$2년생 $1씨는 $3월 $4일에 태어났어요");
		
		System.out.println(res);
}
	
}
```

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Insert title here</title>
</head>
<body>
	<h1>독수리 5형제</h1>
	
	<h2>염호준 아찌</h2>
	항상 뭔가 열심히 하는데.. 뭐를 하는걸까??
	
	<h2>송인범 아저씨</h2>
	Java 빼고 천재
	<h3>오성현 오빠</h3>
	성격은 좋은데.. 공부는 열시히 안하고 도망만 다녀요.
	
	<h4>김지원 누나</h4>
	남친때문에 공부를 열심히 안해요
	
	<h5>심이안 언니</h5>누나는 설 전날 <h5>나온다고 했는데..</h5> 안 나왔죠..
	공부는 안하고 매일 도망만 다녀요... 술은 너무 좋아해요.	
	
	<h1>쿠데타 오빠</h3>			
	구글링을 너무 좋아해요....  문제를 이해하고 풀어야 하는데.	
	
</body>
</html>



find : <h[1-5]>(.+)</h[1-5]>
repl : <li>$1


find : <(h[1-5])>(.+)</\1>
repl : <li>$1

-non greedy
find : <(h[1-5])>(.+)</\1>
repl : <li>$2 $1

	 	역참조 \n : 앞의 그룹과 동일, \1 은 앞의 첫 번째 그룹과 동일
	 	
	 	non-greedy : 한정자 뒤에 ?가 사용될 경우
	 	정규표현식의 한정자는 패턴에 맞는 최대 범위를 찾아서 욕심이 많다(Greedy)
	 	그걸 없애기 위해 non-greedy 하게 검색(최소로)


```


### 11.11 Arrays 클래스

```js
package day29;

import java.util.List;
import java.util.Arrays;

public class Ex14Arrays {

	public static void main(String[] args) {
		int[] arr = {23, 45, 55,24, 78, 90};
		System.out.println("arr = " + arr);
		//arr = [I@2a139a55
		System.out.println("Arrays.toString = " + Arrays.toString(arr));
		//Arrays.toString = [23, 45, 55, 24, 78, 90]
		
		int[] clone = Arrays.copyOf(arr, 10);
		System.out.println("Arrays.toString = " + Arrays.toString(clone));
		//Arrays.toString = [23, 45, 55, 24, 78, 90, 0, 0, 0, 0]
		
		Arrays.fill(clone, 2, 6, 44);
		System.out.println("clone.toString = " + Arrays.toString(clone));
		//clone.toString = [23, 45, 44, 44, 44, 44, 0, 0, 0, 0]
		
		Arrays.sort(clone);
		System.out.println("clone.toString = " + Arrays.toString(clone));
		//clone.toString = [0, 0, 0, 0, 23, 44, 44, 44, 44, 45]
		
		System.out.println("-------------------------");
		
		Member[] members = {
				new Member("심이안", 32),
				new Member("김지원", 31),
				new Member("오성현", 28),
				new Member("송인범", 37),
				new Member("염호준", 38)	
		};
		//Comparable 을 구현해야됨
		Arrays.sort(members);
		System.out.println("members.toString" + Arrays.toString(members));
//		members.toString[Member [name = 오성현, age = 28],
//		                 Member [name = 김지원, age = 31],
//		                 Member [name = 심이안, age = 32],
//		                 Member [name = 송인범, age = 37],
//		                 Member [name = 염호준, age = 38]]
//		
		
		
		arr = new int[] {23, 45, 55, 24, 78, 90, 67, 43};
		int idx = Arrays.binarySearch(arr, 67);
		System.out.println("idx" + idx);
//		idx-5
		
		Arrays.sort(arr);
		idx = Arrays.binarySearch(arr, 67);
		System.out.println("arr.toString = " + Arrays.toString(arr));
//		arr.toString = [23, 24, 43, 45, 55, 67, 78, 90]
		System.out.println("idx" + idx);
//		idx5
		
		
		//배열의 단점 : 추가, 삭제 등 불편함
		List<String> list = Arrays.asList("홍길동", "밀키스", "놀자");
		System.out.println("list.size = " + list.size());
//		list.size = 3
		System.out.println("list = " + list);
//		list = [홍길동, 밀키스, 놀자]
		System.out.println("get(1) = " + list.get(1));
//		get(1) = 밀키스
		
		
	}

}

```
```js
package day29;

public class Member implements Comparable<Member>{
	String name;
	//int age;
	Integer age;
	
	public Member(String name) {
		this.name = name ;
	}
	
	public Member(String name, int age) {
		super();
		this.name = name;
		this.age = age;
	}
	
	@Override
	public int compareTo(Member o) {
		//23 - 25
		return this.age - o.age;
	}

	@Override
	public String toString() {
		return "Member [name = " + name + ", age = " + age + "]";
	}
	
	
	
}

```



### 11.12 Wrapper 클래스
```js
package day29;

public class Ex15Wrapper {

	public static void main(String[] args) {
		//DB테이블에 mem_age : NEMBER : NULL
		//Member 객체에 age(int) 널을 담을 수 있나??
		//반대로 화면에서 나이를 입력받지 않고 DB에 저장할 경우
		//null로 저장 안 되고 0으로 저장되는 문제가 발생
		
		Member mem = new Member("한석규", 34);
		System.out.println("mem = " + mem);
//		mem = Member [name = 한석규, age = 34]
		
		mem.name = null;
		mem.age = null; //오류
		System.out.println("mem = " + mem);
//		mem = Member [name = null, age = null]
		
		
//		//Wrapper 클래스 생성
//		Integer age = new Integer("1004");
//		Integer age = Integer.valueOf(1004);
		Integer age = 1004;  //실제로는 이렇게(자동 박싱)
		int age2 = 1004;
		System.out.println(age);
		
		//기본형으로 꺼낼 때 (언박싱) 기본타입 + Value();
		//int a2 = age.intValue();
		int a2 = age; //자동 언박싱
		System.out.println(a2);
		Integer a = 35 ;
		Integer b = 35 ;
		Integer c = 350 ;
		Integer d = 350 ;
		
		//래퍼객체는 == 으로 비교 안 됨. 단 -128~ + 127 까지는 == 가능
		System.out.println("a==b " + (a == b));	//a==b true
		System.out.println("c==d " + (c == d));	//c==d false
		System.out.println("c.equals(d) = " +  c.equals(d)); //c.equals(d) = true
		
		
		
	}

}

```
### 11.13 Math, Random 클래스
```js
package day29;

public class Ex16Math {

	public static void main(String[] args) {
		double a = 74.69;
		System.out.println("round = " + Math.round(a));
		System.out.println("ceil = " + Math.ceil(a));
		System.out.println("random = " + Math.random());
		// 오라클의 trunc 함수를 구현하고 싶음
		//745263 myTrunc(745263, 2) = 745200
		//745263 myTrunc(745263, 3) = 745000
		int b = 745263;
		System.out.println("myTrunc = " + myTrunc(b, 3));
		//System.out.println(Integer.toBinaryString(b));
		
	}
```




## 15. Collection(다시 정리)

- TreeMap
```js
package day32;

import java.util.Map;
import java.util.TreeMap;
//특정 Map.Entry 찾기
public class TreeMapExample1 {

	public static void main(String[] args) {
		//키로 String 탑을 사용하고 값으로 Integer 타입을 사용하는 TreeMap을 다음과 같이 생성
		TreeMap<Integer, String> scores = new TreeMap<Integer, String>();
		scores.put(new Integer(87), "홍길동");
		scores.put(new Integer(98), "이동수");
		scores.put(new Integer(75), "박길순");
		scores.put(new Integer(95), "신용권");
		scores.put(new Integer(80), "김자바");
		
		Map.Entry<Integer, String> entry = null;
		
		entry = scores.firstEntry();
		System.out.println("가장 낮은 점수 : " + entry.getKey() + " - " + entry.getValue());
		
		entry = scores.lastEntry();
		System.out.println("가장 높은 점수 : " + entry.getKey() + " - " + entry.getValue());
		
		entry = scores.lowerEntry(new Integer(95));
		System.out.println("95점 아래 점수 : " + entry.getKey() + " - " + entry.getValue());
		
		entry = scores.higherEntry(new Integer(95));
		System.out.println("95점 위의 점수 : " + entry.getKey() + " - " + entry.getValue());
		
		entry = scores.floorEntry(new Integer(95));
		System.out.println("95점 이거나 바로 아래 점수 : " + entry.getKey() + " - " + entry.getValue());
		
		while(!scores.isEmpty()) {
			entry = scores.pollFirstEntry();
			System.out.println(entry.getKey() + " - (" + entry.getValue() + " 남은 객체 수 : " +
			scores.size() + ")");
			
//			가장 낮은 점수 : 75 - 박길순
//			가장 높은 점수 : 98 - 이동수
//			95점 아래 점수 : 87 - 홍길동
//			95점 위의 점수 : 98 - 이동수
//			95점 이거나 바로 아래 점수 : 95 - 신용권
//			75 - (박길순 남은 객체 수 : 4)
//			80 - (김자바 남은 객체 수 : 3)
//			87 - (홍길동 남은 객체 수 : 2)
//			95 - (신용권 남은 객체 수 : 1)
//			98 - (이동수 남은 객체 수 : 0)
		}
	}
}

```

- TreeSet1
```js
package day32;

import java.util.TreeSet;
//15.5.2 TreeSet
//특정 객체 찾기
public class TreeSetExample1 {

	public static void main(String[] args) {
		TreeSet<Integer> scores = new TreeSet<Integer>();
		scores.add(new Integer(87));
		scores.add(new Integer(98));
		scores.add(new Integer(75));
		scores.add(new Integer(95));
		scores.add(new Integer(80));
		
		Integer score = null;
		
		score = scores.first();
		System.out.println("가장 낮은 점수 : " + score); //가장 낮은 점수 : 75

		score = scores.last();
		System.out.println("가장 높은 점수 : " + score); //가장 높은 점수 : 98
		
		score = scores.lower(new Integer(95));
		System.out.println("95점 아래 점수 : " + score); // 95점 아래 점수 : 87

		score = scores.higher(95);
		System.out.println("95점 위의 점수 : " + score); // 95점 위의 점수 : 98
		
		score = scores.floor(new Integer(95));
		System.out.println("95점 이거나 바로 아래 점수 : " + score); // 95점 이거나 바로 아래 점수 : 95
		
		score = scores.ceiling(new Integer(85));
		System.out.println("85점 이거나 바로 위의 점수 : " + score); // 85점 이거나 바로 위의 점수 : 87
		
		while(!scores.isEmpty()) {
			score = scores.pollFirst(); //pollFirst : 제일 낮은 객체를 꺼내오고 컬렉션에서 제거
			System.out.println(score + "(남은 객체 수 : " + scores.size() + ")");
//			75(남은 객체 수 : 4)
//			80(남은 객체 수 : 3)
//			87(남은 객체 수 : 2)
//			95(남은 객체 수 : 1)
//			98(남은 객체 수 : 0)	
		}

		while(!scores.isEmpty()) {
			score = scores.pollLast(); //pollLast : 제일 높은 객체를 꺼내오고 컬렉션에서 제거
			System.out.println(score + "(남은 객체 수 : " + scores.size() + ")");
//			98(남은 객체 수 : 4)
//			95(남은 객체 수 : 3)
//			87(남은 객체 수 : 2)
//			80(남은 객체 수 : 1)
//			75(남은 객체 수 : 0)
		}
	}
}

```

- TreeSet2
```js
package day32;

import java.util.NavigableSet;
import java.util.TreeSet;
//객체 정렬하기
public class TreeSetExample2 {

	public static void main(String[] args) {
		TreeSet<Integer> scores = new TreeSet<Integer>();
		scores.add(new Integer(87));
		scores.add(new Integer(98));
		scores.add(new Integer(75));
		scores.add(new Integer(95));
		scores.add(new Integer(80));
		
		NavigableSet<Integer> descendingSet = scores.descendingSet(); //내림차순으로 정렬
		for(Integer score : descendingSet) {
			System.out.print(score + " "); //98 95 87 80 75
		}
		System.out.println();
		
		NavigableSet<Integer> ascendingSet = descendingSet.descendingSet(); //오름차순으로 정렬
		for(Integer score : ascendingSet) {
			System.out.print(score + " "); //75 80 87 95 98
		}
	}

}
```

- TreeSet3
```js
package day32;

import java.util.NavigableSet;
import java.util.TreeSet;

public class TreeSetExample3 {

	public static void main(String[] args) {

		TreeSet<String> treeSet = new TreeSet<String>();
		treeSet.add("apple");
		treeSet.add("forever");
		treeSet.add("description");
		treeSet.add("ever");
		treeSet.add("zoo");
		treeSet.add("base");
		treeSet.add("guess");
		treeSet.add("cherry");
		
		System.out.println("[c~f 사이의 단어 검색]");
		NavigableSet<String> rangeSet = treeSet.subSet("c", true, "f", true); //c <= 검색단어 <= f
														  // 시작 객체, 포함여부, 끝 객체, 포함여부
		for(String word : rangeSet) {
			System.out.println(word);
//			[c~f 사이의 단어 검색]
//					cherry
//					description
//					ever
		}
	}
}

```

- DB랑 연결
```js
package day32;

import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.ResultSet;
import java.sql.SQLException;
import java.sql.Statement;

public class Ex02DBbasic {

	public static void main(String[] args) {

		try {
			//드라이버 로드(적재)
			//로드가 되어야 DB연결 정보를 파악할 수 있다.
			Class.forName("oracle.jdbc.driver.OracleDriver");
			Connection conn = null;
			Statement stmt = null;
			ResultSet rs = null;
			
			// DriverManager 를 통해서 커넥션 구하기
			// Oracle : thin, oci 2개의 접근방법 존재
			conn = DriverManager.getConnection(
					"jdbc:oracle:thin:@localhost:1521:xe", "java", "oracle");
			
			stmt = conn.createStatement();
			//select 문이면 executeQuery,
			//select 문이 아니면 executeUpdate
			rs = stmt.executeQuery("select * from member3");
			//이차워적인 파일에 첫 커서(BOF : Begin Of File)
			//이동 : first, last, previous, next, absolute
			//기본옵션으로 구매했기해 next만 된다.
			while(rs.next()) { //EOF ? : End Of File에 다다르면 false리턴
				//현재 커서위치에서 필드인덱스, 필드명으로 접근 가능
				System.out.print(rs.getString(1) + ", "); //1base(0 base 아님)
				System.out.print(rs.getString("mem_id") + ", ");
				System.out.print(rs.getString("mem_name") + ", ");
				//요청타입으로 꺼내면 알아서, 단 오류나면 에러발생
				System.out.print(rs.getString("mem_mileage") + ", "); //문자로
				System.out.print(rs.getShort("mem_mileage") + ", "); //Short
				System.out.print(rs.getInt("mem_mileage") + ", "); //int
				System.out.println();

			}
			//사용자 자원 해제
			if(conn != null) conn.close(); // 커넥션 반납이 제일 중요
			
		} catch (ClassNotFoundException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		} catch (SQLException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		}
	}

}
```




## JDBC
### JDBC 주로 사용되는 클래스

1. connection : DB 연결을 하는 객체
2. Statement : SQL 구문을 처리하는 객체 - 보안에 취약, 사용하기 불편하여 거의 사용 안 한다.

3. Statement의 단점을 보완하기 위해 아래의 객체들을 사용
  (1)PreparedStatement : 가장 많이 사용
  (2)CallableStatement : 호출(저장프로시저 호출할 때 주로 사용됨)
 
4. ResultSet : 결과객체(Select문)
5. ResultSetMetadata : 결과개체 메타정보(컬럼명, 사이즈, not null) 출력
 
### Statement의 단점
1. 보안에 취약 -> SQL Injection 공격 대상, 그래서 Statement 사용 금지
2. 작은따옴표(') 처리를 위해 replaceAll('   ''   ')
3. 동일 구문 실행시 불편

### DAO, DTO 패턴 (Data Access Object, Data Transfer Object)
- 반복되는 쿼리작업을 효율적으로 관리하기 위해
- DB 테이블과 연관된 작업을 처리하는 전담 클래스 -> DAO
- DAO 패턴 : 하나의 메서드는 하나의 쿼리만 처리
- DTO : 조회된 정보(ResultSet) 를 다른 자바에서 사용할 수 없다. 그래서 조회된 결과정보를 자바객체에 담아서 리턴하거나 어플리케이션에서 입력받은 정보를 DB에 보내기 위해 사용하는 자바객체

### 사용자의 정보, DB의 정보를 담는 객체  
- VO(Value Object), DTO(Data Transfer Object), domain 객체, Java Bean(표준) 객체, Form 객체
- 위 용어가 서로 똑같지는 않지만, 거의 유사한 용도의 객체로 인식하면 된다.


```js
package day33;

import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.ResultSet;
import java.sql.SQLException;
import java.sql.Statement;
import java.util.Scanner;

public class Ex03Statement {
	public static void main(String[] args) {

		Connection conn = null;
		Statement stmt = null;
		ResultSet rs = null;
		Scanner sc = new Scanner(System.in);

		try {
			Class.forName("oracle.jdbc.driver.OracleDriver");
			conn = DriverManager.getConnection(
					"jdbc:oracle:thin:@192.168.20.29:1521:xe", "java", "oracle");
			System.out.println("검색 회원 ID : ");
			String id = sc.nextLine();
			String sql = "SELECT * FROM member3 WHERE mem_id =" + "'"
								+ id.replaceAll("'", "''") + "'";
			System.out.println("sql = " + sql);

			stmt = conn.createStatement();
			rs = stmt.executeQuery(sql);

			// PK 조회이므로 while 일 필요없음

			if(rs.next()) {
				System.out.println("회원이 조회되었습니다.");
				System.out.println("ID = " + rs.getString("mem_id"));
				System.out.println("Name = " + rs.getString("mem_name"));
				System.out.println("Bir = " + rs.getString("mem_bir"));

			}else {
				System.out.println("해당 회원이 존재하지 않습니다.");
			}
			System.out.println("------------------------");
			System.out.println("두 번째 검색 회원 ID : ");
			id = sc.nextLine();
			sql = "SELECT * FROM member3 WHERE mem_id =" + "'"
					+ id.replaceAll("'", "''") + "'";
			System.out.println("2 sql = " + sql);
			rs = stmt.executeQuery(sql);
			if(rs.next()) {
				System.out.println("2 회원이 조회되었습니다.");
				System.out.println("ID = " + rs.getString("mem_id"));
				System.out.println("Name = " + rs.getString("mem_name"));
				System.out.println("Bir = " + rs.getString("mem_bir"));

			}else {
				System.out.println("2 해당 회원이 존재하지 않습니다.");
			}

		} catch (SQLException | ClassNotFoundException e) {
			System.out.println("작업 중 오류 발생: " + e.getMessage());
			e.printStackTrace();
		} finally {
			if(rs != null) try {rs.close();} catch(SQLException e) {}
			if(stmt != null) try {rs.close();} catch(SQLException e) {}
			if(conn != null) try {rs.close();} catch(SQLException e) {}
		}
	}
}
```

```js
package day33;

import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.PreparedStatement;
import java.sql.ResultSet;
import java.sql.SQLException;
import java.sql.Statement;
import java.util.Scanner;

public class Ex04PreparedStatement {
	public static void main(String[] args) {
		
		
		Connection conn = null;
		
		PreparedStatement pstmt = null;
		ResultSet rs = null;
		Scanner sc = new Scanner(System.in);
		String sql = "SELECT * FROM member3 WHERE mem_id = ?";
		
		try {
			Class.forName("oracle.jdbc.driver.OracleDriver");
			conn = DriverManager.getConnection(
					"jdbc:oracle:thin:@192.168.20.29:1521:xe", "java", "oracle");
			System.out.println("검색 회원 ID : ");
			String id = sc.nextLine();
			
			pstmt = conn.prepareStatement(sql);
			pstmt.setNString(1, id); // 1번 물음표(매개변수)에 Id를 문자로
			rs = pstmt.executeQuery();
//			stmt = conn.createStatement();
//			rs = stmt.executeQuery(sql);
			
			// PK 조회이므로 while 일 필요없음
			if(rs.next()) {
				System.out.println("회원이 조회되었습니다.");
				System.out.println("ID = " + rs.getString("mem_id"));
				System.out.println("Name = " + rs.getString("mem_name"));
				System.out.println("Bir = " + rs.getString("mem_bir"));

			}else {
				System.out.println("해당 회원이 존재하지 않습니다.");
			}
			System.out.println("------------------------");
			System.out.println("두 번째 검색 회원 ID : ");
			id = sc.nextLine();
			pstmt.setNString(1, id);
			rs = pstmt.executeQuery();
			// rs = stmt.executeQuery(sql);
			
			if(rs.next()) {
				System.out.println("2 회원이 조회되었습니다.");
				System.out.println("ID = " + rs.getString("mem_id"));
				System.out.println("Name = " + rs.getString("mem_name"));
				System.out.println("Bir = " + rs.getString("mem_bir"));

			}else {
				System.out.println("2 해당 회원이 존재하지 않습니다.");
			}

		} catch (SQLException | ClassNotFoundException e) {
			System.out.println("작업 중 오류 발생: " + e.getMessage());
			e.printStackTrace();
		} finally {
			if(rs != null) try {rs.close();} catch(SQLException e) {}
			if(pstmt != null) try {rs.close();} catch(SQLException e) {}
			if(conn != null) try {rs.close();} catch(SQLException e) {}
		}
	}
}
```

```js
package day33;

import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.PreparedStatement;
import java.sql.ResultSet;
import java.sql.SQLException;
import java.sql.Statement;
import java.util.Scanner;

public class Ex05WhyUsePreparerd {
	public static void main(String[] args) {

		PreparedStatement pstmt = null;
		Connection conn = null;
		Statement stmt = null;
		ResultSet rs = null;
		Scanner sc = new Scanner(System.in);

		try {
			Class.forName("oracle.jdbc.driver.OracleDriver");
			conn = DriverManager.getConnection(
					"jdbc:oracle:thin:@192.168.20.29:1521:xe", "java", "oracle");
			System.out.println("검색 회원 ID : ");
			String id = sc.nextLine();
			
			//statement로 동일 작업
			String sql = "SELECT * FROM member3 WHERE mem_id =" + "'" + id + "'";
			System.out.println("sql = " + sql);
			stmt = conn.createStatement();
			rs = stmt.executeQuery(sql);

			// PK 조회이므로 while일 필요없음
			if(rs.next()) {
				System.out.println("회원이 조회되었습니다.");
				System.out.println("ID = " + rs.getString("mem_id"));
				System.out.println("Name = " + rs.getString("mem_name"));
				System.out.println("Bir = " + rs.getString("mem_bir"));

			}else {
				System.out.println("해당 회원이 존재하지 않습니다.");
			}
			System.out.println("------------------------");
			System.out.println("두 번째 검색 회원 ID : ");
			id = sc.nextLine();
			sql = "SELECT * FROM member3 WHERE mem_id =" + "'"
					+ id.replaceAll("'", "''") + "'";
			System.out.println("2 sql = " + sql);
			sql = "SELECT * FROM member3 WHERE mem_id = ? " ;
			System.out.println("2 sql = "  + sql);
			pstmt = conn.prepareStatement(sql);
			pstmt.setString(1, id);
			rs = pstmt.executeQuery();
			
			
			if(rs.next()) {
				System.out.println("2 회원이 조회되었습니다.");
				System.out.println("ID = " + rs.getString("mem_id"));
				System.out.println("Name = " + rs.getString("mem_name"));
				System.out.println("Bir = " + rs.getString("mem_bir"));

			}else {
				System.out.println("2 해당 회원이 존재하지 않습니다.");
			}
			System.out.println("-----------------------");

			
		} catch (SQLException | ClassNotFoundException e) {
			System.out.println("작업 중 오류 발생: " + e.getMessage());
			e.printStackTrace();
		} finally {
			if(rs != null) try {rs.close();} catch(SQLException e) {}
			if(stmt != null) try {rs.close();} catch(SQLException e) {}
			if(conn != null) try {rs.close();} catch(SQLException e) {}
			if(pstmt != null) try {rs.close();} catch(SQLException e) {}
		}
	}
}
```





