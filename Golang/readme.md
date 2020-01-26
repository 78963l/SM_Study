# GoLang
### [(main)](/readme.md) 
* * *
:large_blue_diamond:**변수**:large_blue_diamond:<br>
- **기본문법**<br>
<practice.go><br>
package main<br>
import "fmt" // (format)<br>
func main() {<br>
　fmt.Print("Hello Go~")<br>
}<br>
실행) go run practice.go<br>
출력) Hello Go~<br><br>
- **변수**<br>
var -> 키워드 (variable - 변수를 의미)<br>
var a int = 3 // (변수 (선언, 초기화))<br>
var b int // (변수 선언)<br>
b = 4 // (변수 초기화)<br>
fmt.Println(a + b)<br><br>
- **변수선언방법**<br>
방법1. var n1 int = 1<br>
방법2. var n1 = 1<br>
방법3. n1 := 1<br>
- **변수여러개선언방법**<br>
방법1. var n1,n2 int = 1, 2<br>
방법2. var (n1,n2 int = 1, 2)<br>
방법3. n1, n2 := 1, 2.6<br><br>
- **데이터 타입**<br>
**1. bool 타입**<br>
bool -> 1byte<br>
**2. 문자열 타입**<br>
string -> 문자열에 따라 다름<br>
UTF-8 영문은 1byte, 한글은 2~3byte<br>
**3. 정수형 타입**<br>
int8 -> 1byte<br>
int16 -> 2byte<br>
int32 -> 4byte<br>
int64 -> 8byte<br>
int -> 컴퓨터의 비트수에 따라 다름(4byte or 8byte)<br>
**4. 실수형 타입**<br>
float32 -> 4byte<br>
float64 -> 8byte<br><br>
- **상수 선언**<br>
const age1 = 20<br>
const age2 // 에러<br>
※ const는 반드시 초기화를 해줘야됨.<br>
**(상수 여러개 선언)**<br>
const (<br>
　a = 0<br>
　b = 1<br>
)<br>

:large_blue_diamond:**조건문**:large_blue_diamond:<br>
- **if 문법1**<br>
if 조건문 {<br>
　명령문1<br>
} else if 조건문{<br>
　명령문2<br>
} else {<br>
　명령문3<br>
}<br><br>
ex)<br>
a := 5<br>
if a == 3 {<br>
    명령문1<br>
} else if a == 4 {<br>
    명령문2<br>
} else{<br>
    명령문3<br>
}<br><br>
- **if 문법2**<br>
if 초기화; 조건문 {<br>
　명령문1<br>
} else if 조건문{<br>
　명령문2<br>
} else {<br>
　명령문3<br>
}<br><br>
ex)<br>
if val := 1; val != 1 {<br>
    fmt.Println("1이 아닙니다.")<br>
} else{<br>
    fmt.Println("1입니다.")<br>
}<br><br>
- **switch 문법**<br>
switch x {<br>
　case 1:<br>
　　명령어1 <br>
　case 2:<br>
　　명령어2 <br>
　default:<br>
　　명령어3 <br>
}<br>
※ fallthrough를 사용하면 C나 C#처럼 밑에 있는 명령어들 실행 가능.<br>
switch x {<br>
　case 1:<br>
　　명령어1 <br>
　　fallthrough<br>
　case 2:<br>
　　명령어2 <br>
　　fallthrough<br>
　default:<br>
　　명령어3 <br>
}<br>

:large_blue_diamond:**반복문**:large_blue_diamond:<br>
- **for 문법**<br>
for 초기화; 조건문; 증감문 {<br>
　명령문<br>
}<br><br>
ex)<br>
func main(){<br>
　var i int<br>
　for i = 0; i < 10; i++ {<br>
　　fmt.Println(i)<br>
　}<br>
　fmt.Println("최종 i 값:", i)<br>
}<br>
최종 i값은?) 10<br><br>