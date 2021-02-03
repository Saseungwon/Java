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








