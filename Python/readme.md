# Python
### [(main)](/readme.md) 
* * *
- :large_blue_diamond: **주석,변수,Print등 한글사용시 추가해야함.**  
#coding: euc-kr  또는 #coding: utf-8    
<br>  
  
- **예약어 확인 ---------------------------------------------------------------**  
import keyword  
keyword.kwlist  
<br>  
  
- **현재 사용 변수 이름알기 ---------------------------------------------------------------**  
dir()  
<br>  
  
- **문자열 포매팅 ---------------------------------------------------------------**  
str = 'Hello'  
'%s Python' % str  
<br>  
  
- **대문자 관련 메소드 ---------------------------------------------------------------**  
1. **첫문자만 영문으로 변경**  
s = "hello Python"  
s.capitalize()  
출력) "Hello Python"  
    
2. **전부 대문자 변경**  
s.upper()  
출력) "HELLO PYTHON"  
    
3. **전부 소문자 변경**  
s.lower()  
출력) "hello world"  
  
4. **소문자인지 검사**  
s.islower()  
출력) True  
  
5. **대문자인지 검사**  
s.isupper()  
출력) False  
  
6. **문장의 모든 단어 첫문자를 대문자로 변경**  
s = "hello world"  
s.title()  
출력) "Hello Wolrd"  
  
7. **대문자는 소문자, 소문자는 대문자로 변경**  
s = "hEllO wORld"  
s.swapcase()  
출력) "HeLLo WorLD"  
<br>  
  
- **문자 검색 관련 메소드 ---------------------------------------------------------------**  
1. **단어가 몇개가 있는지 개수를 나타냄**  
s = "This is Python"  
s.count('this')  
출력) 1  
  
2. **python이라는 단어가 몇번째 인덱스로 시작하는지 찾음**  
s.find('Python')  
출력) 8  
※ 없으면 -1 을 반환  
s.index('Python')  
출력) 8  
※ 차이점 (없으면 -1을 반환하지 않고 에러를 냄)  
<br>  
  
 - **문자 치환 관련 메소드 **  
1. **양쪽 공백 지우기, 원하는 문자 지우기**  
s = " center "  
s.strip()  
출력) "center"  
s = "------center----"  
s.strip(-)  
출력) "center"  

2. **문자 대치**  
s = "Hello Python"  
s.replace("Hello", "Maya")  
출력) "Maya Python"  
<br>  
  
- **문자 분리 관련 메소드 ---------------------------------------------------------------**  
1. **list 문자열을 ':' 기준으로 조합**  
s = "Hello Python"  
':'.join(s.split())  
출력) "Hello:Python"  

2. **'y' 기준으로 분리**  
s = "Hello Python"  
s.split(y)  
출력) ["Hello P","thon"]  
<br>  
  
- **기타 문자 메소드**  
1. **양쪽을 공백으로 채우며 50개 문자를 중앙기준으로 배열**  
s = "Hello Python"  
s.center(50)  
출력) "5o개 공백... Hello Python 50개 공백..."  

2. **양쪽을 -으로 채우며 50개 문자를 중앙기준으로 배열**  
s = "Hello Python"  
s.center(50, '-')  
출력) "5o개 ---... Hello Python 50개 ---..."  
  
3. **왼쪽기준으로 50개 문자를 -으로 채우기**  
s = "Hello Python"  
s.ljust(50, '-')  
출력) "Hello Python 50개 ---..."  

4. **오른쪽기준으로 50개 문자를 -으로 채우기**  
s = "Hello Python"  
s.rjust(50, '-')  
출력) " 50개 ---... Hello Python"  
  
5. **탭을 5개 공백으로 채우기**  
"Hello\t Python".expandtabs(5)   
출력) "Hello\t\t\t\t\t Python"  

6. **숫자로 된 문자열인지 검사**  
"1234".isdigit()  
출력) True  
  
7. **영문자로 된 문자열인지 검사**  
"MAYA".isalpha()  
출력) True  
  
8. **영문자와 숫자인지 검사**  
"MAYA".isalnum()  
출력) True  
  
9. **4개의 '0'을 채워 페딩**  
"12".zfill(4) or "%04d" % 12  
출력) "0012"  
<br>  
  
- **조건문 관계연산 지원**  
1 < 3 < 5  
출력) True  
※ 단 mel이나 Maya expression은 풀어써줘야함 1 < 3 && 3 < 5  
<br>  
  
- **not 논리 연산**  
not 1 < 4  
출력) False  
<br>  
  
- **in 관계 연산**  
st = "abcd"  
'a' in st  
출력) True  
b = [1,2,3,4]  
4 in b  
출력) True  
<br>  
  
- **변수 지우기**  
a = 1  
del a  
<br>  
  
- **객체 치환**  
1. Call By Reference  
a = [1, 2, 3]  
b = [4, a, 'b']  
출력) [4, [1, 2, 3], 'b']  
a[1] = 5  
출력) [4, [1, 5, 3], 'b']  

2. Call By Value  
a = [1,2,3]  
import copy  
b = copy.copy(a)  
출력) [1,2,3] 
a[1] = 10  
a출력) [1, 10, 3]  
b출력) [1, 2, 3]  
<br>  
   
- **시퀀스 자료형**  

