# Tip
## [(main)](/readme.md) 
* * *
### python
* * *
- 주석,변수,Print등 한글사용시 추가해야함.  
#coding: euc-kr  또는 #coding: utf-8  
  
- 예약어 확인  
import keyword  
keyword.kwlist  
  
- 현재 사용 변수 이름알기  
dir()  
  
- 문자열 포매팅  
str = 'Hello'  
'%s Python' % str  
  
- 대문자 관련 메소드  
1. 첫문자만 영문으로 변경  
s = "hello Python"  
s.capitalize()  
출력) "Hello Python"  
  
2. 전부 대문자 변경  
s.upper()  
출력) "HELLO PYTHON"  
  
3. 전부 소문자 변경  
s.lower()  
출력) "hello world"  
  
4. 소문자인지 검사  
s.islower()  
출력) True  
  
5. 대분자인지 검사  
s.isupper()  
출력) False  
  
6. 문장의 모든 단어 첫문자를 대문자로 변경  
s = "hello world"  
s.title()  
출력) "Hello Wolrd"  
  
7. 대문자는 소문자, 소문자는 대문자로 변경  
s = "hEllO wORld"  
s.swapcase()  
출력) "HeLLo WorLD"  
  

