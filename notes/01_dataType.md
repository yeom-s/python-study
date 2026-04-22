## 01. 숫자형
### x의 y제곱을 나타내는 ** 연산자
a = 3
b = 4
print(a ** b)       # 81

### 나눗셈 후 나머지를 리턴하는 % 연산자
print(7 % 3)      # 1

### 나눗셈 vs 몫
print(7 / 4)       # 1.75
print(7 // 4)      # 1

#### 헷갈리는 문제
/ vs // vs %


### 미니문제
a = 14 % 3  
b = 14 // 3  
print(f"몫: {b}, 나머지: {a}")      # 몫: 4, 나머지: 2

---
## 02. 문자열 자료형
문자열(String)이란 **문자, 단어 등으로 구성된 문자들의 집합**을 말한다.

### 문자열을 만드는 방법
1. 큰따옴표(" ")  
`"Hello World"`
2. 작은따옴표(' ')  
`'Python is fun'`
3. 큰따옴표 연속 3개  
`"""Life is too short, You need python"""`
4. 작은따옴표 연속 3개  
`'''Life is too short, You need python'''`

#### 문자열 안에 큰/작은따옴표를 포함시키고 싶을 때
1. 작은따옴표 포함  
`"Python's favorite food is perl"`  
출력: Python's favorite food is perl
>>> 큰따옴표가 아닌 작은따옴표로 둘러싼다면 **'Python'이 문자열로 인식**되어 구문 오류 _(SyntaxError: invalid syntax)_ 가 발생한다.
2. 큰따옴표 포함  
`' "Python is very easy." he says.'`  
출력: "Python is very easy." he says.
3. 역슬래시 사용  
- 역슬래시 뒤의 작은따옴표나 큰따옴표는 문자열을 둘어싸는 기호의 의미가 아니라 "나" 자체를 뜻한다.
    `'Python\'s favorite food is perl'`  
출력: Python's favorite food is perl  

    `"\"Python is very easy.\" he says."`  
출력: "Python is very easy." he says.
