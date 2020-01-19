# Python
### [(main)](/readme.md) 
* * *
 :large_blue_diamond:**주석,변수,Print등 한글사용시 추가해야함**:large_blue_diamond:  
#coding: euc-kr  또는 #coding: utf-8    
<br>  
  
 :large_blue_diamond:**예약어 확인**:large_blue_diamond:  
import keyword  
keyword.kwlist  
<br>  
  
 :large_blue_diamond:**현재 사용 변수 이름알기**:large_blue_diamond:  
dir()  
<br>  
  
:large_blue_diamond:**문자열 포매팅**:large_blue_diamond:  
str = 'Hello'  
'%s Python' % str  
<br>  
  
:large_blue_diamond:**대문자 관련 메소드**:large_blue_diamond:  
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
  
:large_blue_diamond:**문자 검색 관련 메소드**:large_blue_diamond:  
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
  
:large_blue_diamond:**문자 치환 관련 메소드**:large_blue_diamond:  
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
  
:large_blue_diamond:**문자 분리 관련 메소드**:large_blue_diamond:  
1. **list 문자열을 ':' 기준으로 조합**  
s = "Hello Python"  
':'.join(s.split())  
출력) "Hello:Python"  

2. **'y' 기준으로 분리**  
s = "Hello Python"  
s.split(y)  
출력) ["Hello P","thon"]  
<br>  
  
:large_blue_diamond:**기타 문자 메소드**:large_blue_diamond:  
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
  
:large_blue_diamond:**조건문 관계연산 지원**:large_blue_diamond:  
1 < 3 < 5  
출력) True  
※ 단 mel이나 Maya expression은 풀어써줘야함 1 < 3 && 3 < 5  
<br>  
  
:large_blue_diamond:**not 논리 연산**:large_blue_diamond:  
not 1 < 4  
출력) False  
<br>  
  
:large_blue_diamond:**in 관계 연산**:large_blue_diamond:  
st = "abcd"  
'a' in st  
출력) True  
b = [1,2,3,4]  
4 in b  
출력) True  
<br>  
  
:large_blue_diamond:**변수 지우기**:large_blue_diamond:  
a = 1  
del a  
<br>  
  
:large_blue_diamond:**객체 치환**:large_blue_diamond:  
1. **Call By Reference**  
a = [1, 2, 3]  
b = [4, a, 'b']  
출력) [4, [1, 2, 3], 'b']  
a[1] = 5  
출력) [4, [1, 5, 3], 'b']  
    
2. **Call By Value**  
a = [1,2,3]  
import copy  
b = copy.copy(a)  
출력) [1,2,3] 
a[1] = 10  
a출력) [1, 10, 3]  
b출력) [1, 2, 3]  
<br>  
   
:large_blue_diamond:**시퀀스 자료형**:large_blue_diamond:  

:small_orange_diamond: 문자열 :small_orange_diamond:  
[<시작수>:<끝수>:간격수>]  
s="hello"  
s[1]  
출력) "e"  
s[3:]  
츨력) "lo"  
s[1:5]  
출력) "ello"  
s[:4]  
출력) "hell"  
s[-1]  
출력) "o"  
s[-4]  
출력) "e"  
h e l l o  
0 1 2 3 4 5
-5 -4 -3 -2 -1 0  
  
:small_orange_diamond:리스트:small_orange_diamond:  
1. **선언**  
li = [1,2,3]  
    
2. **개수**  
len(li)  
출력)3  
    
3. **여러개 추가**  
li + [4,5,6]  
출력) [1,2,3,4,5,6]  
li 출력) [1,2,3]  
li += [4,5,6]  
출력) [1,2,3,4,5,6]  
li 출력) [1,2,3,4,5,6]  
    
4. **한개 추가**  
li.append(7)  
li 출력) [1,2,3,4,5,6,7]  
    
5. **자르기**  
li[1:3]  
출력) [2,3]  
li[::2]  
출력) [1,3,5,7]  
li[::3]  
출력) [1,4,7]  
    
6. **<치환>**  
li[1] = 10  
li 출력) [1,10,3,4,5,6,7]  
    
7. **리스트 자료복사하여 넣기**  
li * 2  
출력) [1,10,3,4,5,6,7,1,10,3,4,5,6,7]  
li 출력) [1,10,3,4,5,6,7]  
li *= 2  
출력) [1,10,3,4,5,6,7,1,10,3,4,5,6,7]  
li 출력) [1,10,3,4,5,6,7,1,10,3,4,5,6,7]  
    
8. **자료있는지 검사**  
10 in li  
출력) True  
    
9. **자료중복 확인**  
li.count(4)  
출력) 2  
    
10. **인덱스로 삭제**  
del li[1]  
li 출력) li 출력) [1,3,4,5,6,7,1,10,3,4,5,6,7]  
<slicing 으로 삭제>  
li[4:6]  
출력)[6,7]  
li[4:6] = []  
li 출력) [1,3,4,5,1,10,3,4,5,6,7]  
    
11. **특정자료 index 구하기**  
li.index(10)  
출력) 7  

:small_orange_diamond:Range:small_orange_diamond:  
range(<시작수>:<끝수>:<증가수>)  
range(5)  
for문 출력) [0,1,2,3,4]  
<br>
range(5,10)  
for문 출력) [5,6,7,8,9]  
<br>
range(0,10,2)  
for문 출력) [0,2,4,6,8]  
<br>
range(0,-5,-1)  
for문 출력) [0,-1,-2,-3,-4]  
    
:small_orange_diamond:중첩리스트:small_orange_diamond:  
li1 = ['a','b','c']  
li2 = [1,2,li1,3,4]  
li2 출력) [1,2,['a','b','c'],3,4]  
li2[2][1] 출력) "b"  
li2[3] = [11,22,33]  
li2 출력) [1,2,['a','b','c'],[11,22,33]],4]  
    
:small_orange_diamond:리스트 메소드:small_orange_diamond:  
1. **리스트 인덱스로 추가**  
li = ['a','b','c','e']  
li.insert(3, 'd')  
li 출력) ['a','b','c','d','e']  
    
2. **리스트 정렬 반대로**  
li.reverse()
li 출력) ['e','d','c','b','a']  
※ li.sort(reverse=True) 동일.  
    
3. **순서대로 정렬**  
li.sort()  
li 출력) ['a','b','c','d','e']  
※ sort는 리턴값이 없다.  
    
4. **특정 자료 지우기**  
li.remove('c')  
li 출력) ['a','b','d','e']  
    
5. **여러개추가**  
li.extend(['f','g'])  
li 출력) ['a','b','d','e','f','g']  
    
6. **list형으로 추가**  
li.aapend(['f','g'])  
li 출력) ['a','b','d','e',['f','g']]  
    
:small_orange_diamond:리스트 스택:small_orange_diamond:  
1. **데이터 추가**  
li = [1,2,3,4,5]  
li.append(6)  
li 출력) [1,2,3,4,5,6]  
    
2. **데이터 빼기**  
li.pop()  
li 출력) [1,2,3,4,5]  
    
:large_blue_diamond:**Tuple**:large_blue_diamond:  
1. **연산**  
t = ('a','b','c','d')  
t + ('e','f')  
출력) ('a','b','c','d','e','f')  
t * 2  
출력) ('a','b','c','d','a','b','c','d')  
    
2. **포매팅**  
h,m = "hello", "maya"  
h 출력) "hello"  
m 출력) "maya"  
print "%s~~ %s!!!" % (h, m)  
출력) hello~~ maya!!!  
    
:large_blue_diamond:**Dictionary**:large_blue_diamond:  
:small_orange_diamond:연산:small_orange_diamond:  
obj = {"Cube":"mesh", "Shpere":"nurbs", "Cone":"mesh"}  
    
:small_orange_diamond:검색:small_orange_diamond:  
1. **검색**
obj["Cube"]  
출력) "mesh"  
※key를 넣어야함.(없으면 에러를 냄)  
    
2. **치환**  
obj["Cube"] = "nurbs"  
obj 출력) {"Cube":"nurbs", "Shpere":"nurbs", "Cone":"mesh"}  
    
3. **삭제**  
del obj["Cone"]  
obj 출력) {"Cube":"nurbs", "Shpere":"nurbs"}  
    
4. **자료 개수**  
len(obj)  
출력) 2  
    
:large_blue_diamond:**Dictionary Method**:large_blue_diamond:  
obj = {"Cube":"mesh", "Shpere":"nurbs", "Cone":"mesh"}  
    
1. **key의 리스트 받기**  
obj.keys()  
출력) ["Cube","Shpere","Cone"]  
    
2. **value의 리스트 받기**  
obj.values()  
출력) ["mesh","nurbs","mesh"]  
    
3. **(key와 value)를 리스트형과 튜플형으로 받기**  
obj.items()  
출력) [("Cube":"mesh"), ("Shpere":"nurbs"), ("Cone":"mesh")]  
    
4. **key값 유무**  
"Box" in obj  
출력) True  
※ value값 유무는 다른방식으로 해야함.  
    
5. **value값 유무**  
"mesh" in obj.values()  
출력) True  
    
6. **검색**  
obj.get("Shpere")  
출력) nurbs  
※ 없는 값은 None으로 리턴됨.(기본방식(에러)과 다름)  
obj.get("Hex", "mesh")  
출력) "mesh"  
※ 없는 값이면 지정한 value로 나옴.(단 사전엔 추가x)  
ob.setdefault("Hex", "mesh")
※ 없는 값이면 지정한 value로 나옴.(단 사전엔 추가o)  
    
7. **삭제**  
obj.popitem()  
출력) ("Cone", "mesh")  
※ 사전에는 지워짐.  
obj.pop("Shpere")  
출력) "nurbs"  
※ 사전에는 지워짐.  
    
8. **존재유무**  
obj.has_key("Cube")  
출력) True  
    
9. **특정 key들을 한번에 default값으로 설정**  
obj = dict.fromkeys(["B1","B2","B3"], "mesh")  
obj 출력) {("B1": "mesh", "B2": "mesh", "B3": "mesh"}
