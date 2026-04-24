## 02-1. 숫자형
### - 주요 연산자
__거듭 제곱 (**)__
```
a = 3
b = 4
print(a ** b)       # 81
```

**나머지 (%)**
```
print(7 % 3)      # 1
```

**나눗셈 vs 몫 vs 나머지**
| 연산자 | 설명 | 예시 | 결과 |
|--------|------|------|------|
| `/` | 나눗셈 (소수점 포함) | `7 / 4` | `1.75` |
| `//` | 몫 (정수만)          | `7 // 4` | `1` |
| `%` | 나머지               | `7 % 4` | `3` |

**💡 미니문제**  
• 14를 3으로 나눴을 때, 몫과 나머지를 구하라
>```
>a = 14 % 3  
>b = 14 // 3  
>print(f"몫: {b}, 나머지: {a}")      # 몫: 4, 나머지: 2
>```

---

## 02-2. 문자열 자료형
문자열(String)이란 **문자, 단어 등으로 구성된 문자들의 집합**을 말한다.

### - 문자열을 만드는 방법
```
"Hello World"       # 큰따옴표
'Python is fun'     # 작은따옴표
"""Life is too short, You need python"""    # 큰따옴표 3개
'''Life is too short, You need python'''       # 작은따옴표 3개
```

### - 문자열 안에 큰/작은따옴표를 포함시키고 싶을 때
**방법 1 - 다른 종류의 따옴표로 감싸기**
```
"Python's favorite food is perl"        # 출력: Python's favorite food is perl
' "Python is very easy." he says.'      # 출력: "Python is very easy." he says.
```
> 큰따옴표가 아닌 작은따옴표로 둘러싼다면 **'Python'이 문자열로 인식**되어 구문 오류 _(SyntaxError: invalid syntax)_ 가 발생한다.

**방법 2 - 역슬래시(\\) 사용**  
역슬래시 뒤의 작은따옴표나 큰따옴표는 문자열을 둘어싸는 기호의 의미가 아니라 "나" 자체를 뜻한다.  
```
'Python\'s favorite food is perl'           # 출력: Python's favorite food is perl  
"\"Python is very easy.\" he says."      # 출력: "Python is very easy." he says.
```

### - 이스케이프 코드
| 코드 | 설명 |
|-----|-----|
| `\n` | 문자열 안에서 줄을 바꿀 때 사용 |
| `\t` | 문자열 사이에 탭 간격을 줄 때 사용 |
| `\\` | `\` 를 그대로 표현할 때 사용 |
| `\'` | 작은따옴표 `' '` 를 그대로 표현할 때 사용 |
| `\"` | 큰따옴표 `" "` 를 그대로 표현할 때 사용 |
| `\r` | 캐리지 리턴(줄 바꿈 문자, 커서를 현재 줄의 가장 앞으로 이동)
| `\f` | 폼 피드(줄 바꿈 문자, 커서를 현재 줄의 다음 줄로 이동) |
| `\a` | 벨소리(출력할 때 PC 스피커에서 '삑' 소리가 난다) |
| `\b` | 백 스페이스 |
이 중에서 활용 빈도가 높은 것은 `\n`, `\t`, `\\`, `\'`, `\"` 이다.

### - 문자열 연산하기
**문자열 더하기**
```
a = "Python"
b = " is fun!"
print(a+b)      # Python is fun!
```

**문자열 곱하기**
```
a = "python"
print(a * 2)        # pythonpython
```

**문자열 길이 구하기**  
• 길이는 len 함수를 사용하여 구할 수 있다(공백 문자 포함)   
• len 함수는 print 함수처럼 파이썬의 기본 내장 함수로, 별다른 설정 없이 바로 사용할 수 있다.
```
a = "All we have is now"
print(len(a))   # 18
```

**💡 미니문제**  
• You need python을 문자열로 만들고 길이를 구하라.
>```
>x = "You need python"
>print(len(x))   # 15
>```

### - 문자열 인덱싱과 슬라이싱
**문자열 인덱싱**
```
x = "Try your best rather than be the best"
print(x[2])     # y
print(x[0])    # T
print(x[-1])    # t
```
x[0]: `T`, x[1]: `r`, x[2]: `y`, x[3]: ` `, x[4]: `y`, ⋯  
• 파이썬은 0부터 숫자를 센다.  
• -1은 뒤에서부터 첫 번째 문자, -5는 뒤에서부터 다섯 번째 문자를 뜻한다.

**문자열 슬라이싱**
```
x = "Try your best rather than be the best"
y =  x[0] + x[1] + x[2] + x[3] + x[4] + x[5]
print(y)    # Try yo
```