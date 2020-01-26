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
1. bool 타입<br>
bool -> 1byte<br>
2. 문자열 타입<br>
string -> 문자열에 따라 다름<br>
UTF-8 영문은 1byte, 한글은 2~3byte<br>
3. 정수형 타입<br>
int8 -> 1byte<br>
int16 -> 2byte<br>
int32 -> 4byte<br>
int64 -> 8byte<br>
int -> 컴퓨터의 비트수에 따라 다름(4byte or 8byte)<br>
4. 실수형 타입<br>
float32 -> 4byte<br>
float64 -> 8byte<br>