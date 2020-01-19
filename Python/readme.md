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
li * = 2  
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
    
10. **사전에 사전추가**  
a = {"1":"one","2":"two"}  
b = {"3":"three","4":"four"}  
a.update(b)
a 출력) {'1': 'one', '2': 'two', '3': 'three', '4': 'four'}  
    
11. **사전 지우기**  
a.clear()  
    
12. **사전 대입 (원본, 참조 동일o)**  
a = {"1":"one","2":"two"}  
a = b  
a["2"]="이"  
a 출력) {"1":"one","2":"이"}  
b 출력) {"1":"one","2":"이"}  
    
13. **사전 대입 (원본, 참조 동일x)**    
a = {"1":"one","2":"two"}  
a = b.copy()  
a["2"]="이"  
a 출력) {"1":"one","2":"이"}  
b 출력) {"1":"one","2":"two"}  
    
:large_blue_diamond:**시퀀스 자료형 변환**:large_blue_diamond:  
:small_orange_diamond:list <-> Tuple:small_orange_diamond:  
1. **튜플 -> 리스트 변환**  
tu_ = ('a','b','c')  
li_ = list(tu_)  
li_ 출력) ['a','b','c']  
    
2. **리스트 -> 튜플 변환**  
li_ = ['a','b','c']  
tu_ = tuple(li_)  
tu_ 출력) ('a','b','c')  
    
:small_orange_diamond:dictionary Type Exchange:small_orange_diamond:  
1. **리스트 -> 리스트튜플 변환**  
a_ = ['1','2','3']  
b_ = ['one','two','three']  
zip(a_, b_)  
출력) [('1', 'one'), ('2', 'two'), ('3', 'three')]  
    
2. **리스트 -> 사전 변환**  
a_ = ['1','2','3']  
b_ = ['one','two','three']  
dic(zip(a_, b_))
출력) ['1':'one', '2':two, '3':three]  
    
:large_blue_diamond:**시퀀스 중첩 자료**:large_blue_diamond:  
1. **사전안에 리스트 중첩**  
all = dict.fromkeys(['group_A', 'group_B'])  
all['group_A'] = ['box1', 'box2']  
all['group_B'] = ['sphere1', 'sphere2']  
all 출력) {'group_A': ['box1', 'box2'], 'group_B': ['sphere1', 'sphere2']}  
all['group_B'][1] 출력) 'sphere2'  
    
2. **사전안에 사전 중첩**  
all_grp = dict.fromkeys(['a','b']  
all_grp['a'] = dict.fromkeys(['grp1','grap2'])  
all_grp['b'] = dict.fromkeys(['grp3','grap4'])  
all_grp['a']['grp1'] = dict.fromkeys(['box1', 'box2', 'box3'], 'mesh')  
all_grp['a']['grp2'] = dict.fromkeys(['sphere1', 'sphere2', 'sphere3'], 'nurbs')  
all_grp 출력) {'a': {'grp2':{sphere1:nurbs, "sphere2":nurbs, "sphere3":nurbs}, 'grp1':{'box1':'mesh','box2':'mesh','box3':'mesh'}}, 'b': {'grp3':None, 'grp4':None}}  
all_grp['a']['grp1'] 출력) {'box1':'mesh','box2':'mesh','box3':'mesh'}  
    
:large_blue_diamond:**리스트 내장**:large_blue_diamond:  
**for문 문법**  
for <변수> in <시퀀스>:  
　<명령문>  
***
**while문 문법**  
while <조건>:  
　<명령문>  
***
li_ = [x for x in range(2, 10, 2)]  
for x in li_:  
　print x  
출력) 2 4 6 8  
li_ = ["num:" + x for x in range(2, 10, 2)]  
for x in li_:  
　print x  
출력) num2 num4 num6 num8  
    
:large_blue_diamond:**제어문**:large_blue_diamond:  
**if문 문법**  
if <조건1>:  
<명령문>  
elif <조건2>:  
<명령문>  
else:  
<명령문>  
※ break(만나는 순간 종료), continue(만나는 순간 아래 명령은 실행하지 않고 다시 반복) 가 있음.  
    
:large_blue_diamond:**조건선언**:large_blue_diamond:  
**조건선언 문법**  
<변수> = <값1> if <조건> else <값2>  
ex) v_ = 'true' if 3 < 4 else 'false'  
v_ 출력) true  
if 3 < 4:  
　v_ = 'true'  
else:  
　v_ = 'false'  
***
:large_blue_diamond:**리스트내장**:large_blue_diamond:  
**리스트 안에 for문 명령을 포함**  
list_ = ['a1','2','a3','a4','5']  
v_ = [x for x in list_ if x[0] == 'a']  
v_ 출력) ['a1', 'a3', 'a4']  
※ 리스트내장안에 있는 if조건시 else는 사용 불가!!  
***
**if 조건에는 bool()이 생략 되어있다.**  
if bool(조건):  
ex) if 0:  
print("true")  
else:  
print("false")  
출력) false  
    
:large_blue_diamond:**함수**:large_blue_diamond:  
**함수 문법**  
def <함수이름>(<인자>):  
<명령문>  
return 값  
※인자와 return 값을 안줘도 됨.  
***
def f_():  
return  
※ return 값은 None이 됨.  
***
def f_():  
　return 1, 2  
f_()  
(1,2)  
※ return 값은 Tuple이 됨.  
    
:large_blue_diamond:**지역변수, 전역변수**:large_blue_diamond:  
1. **변수 확인**  
a_ = 1  
def f_():  
　b_ = 2  
　print locals()  
　print globals()  
     
2. **함수안에서 전역변수 사용**  
a_ = 3
def f_():  
　global a_  
a_ += 2  
　return a_  
a_ 출력) 3  
f_()
a_ 출력) 5  
    
3. **재귀함수**  
a_ = 1  
def f_():  
　print("function")  
global a_  
a_ += 1  
if(a < 3):
　f_()  
print(f_())  
출력) function function None  
※ 마지막 None이 나오는 이유는 return 값이 없는 함수이기 때문이다.  
    
4. **인수전달**  
- **가변인수 전달**  
인수개수가 몇개인지 모를때 사용.  
def f_(*var_):  
　return var_  
f_(1)  
출력) (1,)  
f_(1,2,3)  
출력) (1,2,3)  
    
- **키워드 인수 전달**  
def key_word(MAYA_, max_):  
　return MAYA_, max_  
key_word(max_ = 'mxs', MAYA_ = 'Python')  
출력) ('Python', 'mxs')  
    
5. **람다함수**  
한줄의 함수로 return 명령없이 return 함  
**문법**  
lambda <인수> : <리턴방식>  
myf = lambda a, b : a + b  
myf(1, 2)  
출력) 3  
    
6. **함수 인자 넘기기**  
- **list 또는 Tuple로 인수 넘기기**  
def f_(a, b, c):  
　retrun a+b+c  
li_ = [2, 3, 4]  
f_(*li_)  
출력) 9  
tu_ = (100, 200, 300)  
f_(*tu_)  
출력) 600  
    
- **사전형으로 인수 넘기기**  
def f_(a, b, c):  
　return a+b, b+c, c+a  
dic_ = {'a':1, 'b':2, 'c':3}  
f_(**dic_)  
출력) (3, 5, 4)  
    
:large_blue_diamond:**모듈**:large_blue_diamond:  
p.py  
def f_1():  
　return ("function1")  
def f_2():  
　return ("function2")  
basic.py  
import p  
print(p.f_1())  
    
:large_blue_diamond:**PYTHONPATH 환경변수**:large_blue_diamond:  
1. **Python환경변수 확인**  
import sys  
path_ = sys.path  
for i in path_:  
　print(i)  
※ 만약 모듈이 확인한 디렉토리 안에 들어있으면 디렉토리 이동없이 바로 불러 사용가능.  
    
2. **Python환경변수 추가**  
- **1번째 방법**  
import sys  
sys.path.append('C:\\modules')  
※ 경로해제는 sys.path.remove('C:\\modules')  
※ 쉘에서는 append가 안된다.  
- **2번째 방법**  
window  
set PYTHONPATH=.;c:\Python\lib;c:\Python\lib\tkinter  
Linux/MAC(unix systeam)  
setenv = PYTHONPATH .:/usr/local/user/modules lnu
Linux  
~/.cshrc  
    
3. **import 활용**  
import maya.cmds as cmds  
import maya  
dir(maya)  
출력) ['__builtins__', '__doc__', '__file__', '__name__', '__path__', 'cmds', 'mel', 등등..]  
    
4. **from 활용**  
from maya.cmds import *  
sphere()  
※ namespace 없이 명령 사용가능.  
from maya import cmds, mel  
※ 한번에 2개를 불러올 수 도 있음.  
    
4. **reload() 활용**  
첫 import시 내용 수정을 해도 변경되지 않음.  
import value  
reload(value)  
    
5. **__ name __ 활용**  
현재 실행하는 공간의 이름을 알수 있음.  
__ name __  
출력) ' __ main __ '  
module.__ name __  
출력) 'module'  
- golbal 공간에서 사용하는 것을 포함하지 않고 싶을때.  
if __ name __ == ' __ main __ '  
<명령어>  
    
:large_blue_diamond:**클래스(Class)**:large_blue_diamond:  
1. **NameSpace**  
class A:  
　def f1(self):  
　　print 'f1'  
　def f2(self):  
　　print 'f2'  
PracClass = A()  
PracClass.f1() / f1  
PracClass.f2() / f2  
    
2. **클래스 상속**  
class A:  
　　a_ = None  
　　b_ = None  
　　c_ = None  
　　def a(self, x):  
  　　self.a_ = x  
　　　print self.a_, self.b_, self.c_  
　　def b(self, x):  
　　　self.b_ = x  
　　　print self.a_, self.b_, self.c_  
　　def c(self, x):  
　　　self.c_ = x  
　　　print self.a_, self.b_, self.c_  
class1 = A()  
class1.a(1)  
출력) 1 None None  
class1.c(3)  
출력) 1 None 3  
***
class b(A):  
　　　pass  
cb = b()  
cb.a(9)  
출력) 9 None None  
상속이 됨.  
    
3. **클래스 멤버와 인스턴스 멤버**  
