# Tip
### [(main)](/readme.md) 
***
### -- Program --
* [Maya](#1-maya)
* [Nuke](#2-nuke)
* [Houdini](#3-houdini)
* [3DEqualizer](#4-3dequalizer)
* [Tractor](#5-tractor)
* [Unity3D](#6-unity3d)
* [Unreal](#7-unreal)
* [AndroidStudio](#8-androidstudio)
***
### -- Language --  
* [C](#9-c)
* [C++](#10-c)
* [C#](#11-c)
* [Java](#12-java)
* [JavaScript](#13-javascript)
* [TypeScript](#14-typescript)
* [Python](#15-python)
* [GoLang](#16-golang)
* [Html](#17-html)
* [Jsp](#18-jsp)
***
#### 1. Maya
***
***
#### 2. Nuke
***
***
#### 3. Houdini
***
***
#### 4. 3DEqualizer
***
***
#### 5. Tractor
***
***
#### 6. Unity3D
***
:large_blue_diamond:**PlayerPrefs**:large_blue_diamond:<br>
- PlayerPrefs클래스는 유니티에서 제공하는 데이터 관리 클래스.<br>
- int, float, string, bool 타입의 변수를 저장하고 로드할 수 있다.<br>
>PlayerPrefs.SetInt("Age", int.Parse(aa.text));<br>
bb.text = PlayerPrefs.GetInt("Age").ToString();
- DeleteAll : 모든 키값 삭제
- DeleteKey : 키값 삭제
- GetInt : 입력한 int 키값 로드
- GetFloat : 입력한 float 키값 로드
- GetString : 입력한 string 키값 로드
- SetInt : 입력한 int 키값 저장
- SetFloat : 입력한 float 키값 저장
- SetString : 입력한 string 키값 저장
- HasKey : 해당 키의 존재여부를 반환
- Save : 변경된 모든 키값을 저장
- ＊ 보안상 문제가 되므로 중요한 데이터이라면, JSON과 XML을 이용해야 한다.<br><br>
:large_blue_diamond:**Unity의 기본모듈을 가져오지못하는 에러**:large_blue_diamond:<br>
>errorCode) namespace name 'UI' does not exist in the namespace 'UnityEngine' (are you missing an assembly reference?)<br>

※ unity의 버전을 올리거나 dll파일이 사라진 경우.<br>
Assets -> Reimport All<br>
현재 프로젝트를 연 unity의 버전에 따라 dll 파일이 전부 import가 되어 모듈을 가져올 수 있다.<br>
***
#### 7. Unreal
***
***
#### 8. AndroidStudio
***
***
#### 9. C
***
***
#### 10. C++
***
***
#### 11. C#  
***
***
#### 12. Java  
***
***
#### 13. JavaScript  
***
***
#### 14. TypeScript  
***
***
#### 15. Python  
:large_blue_diamond:**메모리 관리를 따로 안해줘도 됨**:large_blue_diamond:<br>
- C/C++ 처럼 메모리를 직접 할당/해제할 필요가 없음.<br>
python에는 Gabage Collection이 있어 자동으로 수집하고 해제함.(java와 동일)<br>
del(변수) 를 이용하여 지우는 함수가 있지만 실제로 메모리에서는 해제하지 않음.<br>
하여 메모리에 문제가 생길 수 있어 None타입으로 변경 후 del함수를 사용하는 것이 바람직함.<br>
* * *  
:large_blue_diamond:**깊은복사,얕은복사(DeepCopy, ShallowCopy)**:large_blue_diamond:<br>
1. DeepCopy<br>
a = [1,2,3]<br>
b = a<br>
a[0] = 5<br>
a 출력) [5,2,3]<br>
b 출력) [5,2,3]<br><br>
2. ShallowCopy<br>
import copy<br>
a = [1,2,3]<br>
b = copy.copy(a)<br>
a[0] = 5<br>
a 출력) [5,2,3]<br>
b 출력) [1,2,3]<br>
* * *
:large_blue_diamond:**false, true 값**:large_blue_diamond:  
- false<br>
"", [],(), {}, 0, None<br>
- true<br>
"aa", [1,2,3], 1<br>
* * *
:large_blue_diamond:**문자열 명령실행**:large_blue_diamond:  
- eval의 string 실행  
>eval('1 + 2')  
3  

>eval('4 < 3')  
False  

>eval('[123, "abc"]')  
[123, "abc"]  

- exec의 string 실행  
>exec('a = 1 + 3')  
a  
4  
※ exec는 eval과 다르게 return을 하지 않는다.

- 변수에 함수처럼 저장이 가능  
c_ = '''  
a = 4  
for x in range(a):  
    print(x)  
'''  
exec(c_)  
0  
1  
2  
3 
* * *
:large_blue_diamond:**줄 바꿔 쓰기**:large_blue_diamond:  
명령어가 길어질 경우  
> import maya.cmds as cmds  
box = cmds.polyCube(height=4,  
width=5,  
depth=2)  

()와 같은 내용 안에 있는 명령은 줄을 바꿔써도 영향을 받지 않는다.  
[]이나 {}도 동일하다.  

만약 ()[]{}와 같은 자료 안의 내용이 아닌 명령 문장은 역슬레쉬 \ 를 이용하여 줄바꾸기가 가능하다.  
* * *
:large_blue_diamond:**한 줄에 여러 명령쓰기**:large_blue_diamond:  
;를 사용하면 한줄에 여러명령을 사용을 할 수 있다.  
>num=1;print num
* * *
:large_blue_diamond:**문자열 실행하기**:large_blue_diamond:  
1. eval의 string 실행
> eval('1+2')  
※ eval은 항상 결과를 return 한다.(mel.eval('sphere')와는 다름)  
2. exec의 string 실행
> exec('sum = 5 + 2')  
> sum  
> 4  
※ eval하고 차이점은 return을 하지 않는다.  
***
***
#### 16. GoLang
:large_blue_diamond:**숫자입출력 예제**:large_blue_diamond:<br>
package main<br><br>
import (<br>
　"bufio" // 읽기<br>
　"fmt"<br>
　"os"      // 쓰기<br>
　"strconv" // 문자열을 숫자로 변경<br>
　"strings" // 문자열 패키지<br>
)<br><br>
func main() {<br>
　fmt.Println("숫자를 입력하세요")<br>
　reader := bufio.NewReader(os.Stdin)<br>
　line, _ := reader.ReadString('\n') // 개행문자가 나올때까지 읽음.(_이것은 이름없는 변수(처리하지않음))<br>
　line = strings.TrimSpace(line)     // 빈공간 없애기<br><br>
　n1, _ := strconv.Atoi(line) // 문자를 숫자로 변경<br><br>
　line, _ = reader.ReadString('\n')<br>
　line = strings.TrimSpace(line)<br><br>
　n2, _ := strconv.Atoi(line)<br><br>
　fmt.Printf("입력하신 숫자는 %d, %d 입니다.", n1, n2)<br>
}<br><br>
입력) 숫자를 입력하세요 <br>
3<br>
5<br>
출력) 입력하신 숫자는 3, 5 입니다.<br>
***
***
#### 17. Html  
***
#### 18. Jsp  
***
