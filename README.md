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