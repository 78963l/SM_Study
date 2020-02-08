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
#### 2. Nuke
***
#### 3. Houdini
***
#### 4. 3DEqualizer
***
#### 5. Tractor
***
#### 6. Unity3D
***
#### 7. Unreal
***
#### 8. AndroidStudio
***
#### 9. C
***
#### 10. C++
***
#### 11. C#  
***
#### 12. Java  
***
#### 13. JavaScript  
***
#### 14. TypeScript  
***
#### 15. Python  
:large_blue_diamond:**메모리 관리를 따로 안해줘도 됨**:large_blue_diamond:<br>
- C/C++ 처럼 메모리를 직접 할당/해제할 필요가 없음.<br>
python에는 Gabage Collection이 있어 자동으로 수집하고 해제함.(java와 동일)<br>
del(변수) 를 이용하여 지우는 함수가 있지만 실제로 메모리에서는 해제하지 않음.<br>
하여 메모리에 문제가 생길 수 있어 None타입으로 변경 후 del함수를 사용하는 것이 바람직함.<br>

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

:large_blue_diamond:**false, true 값**:large_blue_diamond:  
- false<br>
"", [],(), {}, 0, None<br>
- true<br>
"aa", [1,2,3], 1<br>

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
#### 17. Html  
***
#### 18. Jsp  
***
