# JavaScript
### [(main)](/readme.md) 
* * *

:large_blue_diamond:**테스트하기 좋은 사이트**:large_blue_diamond:<br>
- url : https://jsbin.com<br>

:large_blue_diamond:**변수 let & const**:large_blue_diamond:<br>
- let : 변수선언<br>
- let : 상수선언<br>

:large_blue_diamond:**화살표 함수**:large_blue_diamond:<br>
- default
```
function App(){}
```
- arrow
```
const App = ()=>{}
```

:large_blue_diamond:**Export & Import**:large_blue_diamond:<br>
- export : 내보내기<br>
```
#person.js
const person = {name:'이름'}
export default person

#util.js
export const age = 30;
```
- import : 가져오기<br>
```
import person from './person.js'
import {age} from './util.js'
```

:large_blue_diamond:**Class**:large_blue_diamond:<br>
- Class Default
```
class Person {
    constructor(){

    }
    name = '이름'       // Property
    eat = () => {...}   // Method
}
```

- 인스턴스 생성
```
const person = new Person()
person.eat()
```

- class 상속
```
class Person extends Master
```

- class 상속 응용 (ES6)
```
class Human {
    constructor(){
        this.gender = 'male';
    }
    printGender(){
        console.log(this.gender);
    }
}

class Person extends Human{
    constructor(){
        super();
        this.name = 'myName';
        this.gender = 'female';
    }
    printMyName(){
        console.log(this.name);
    }
}

const person = new Person();
person.printMyName();
person.printGender();
```

- class 상속 응용 (ES7)
```
class Human {
    gender = 'male';
    printGender = () => {
        console.log(this.gender);
    }
}

class Person extends Human{
        name = 'myName';
        gender = 'female';
    }
    printMyName = () => {
        console.log(this.name);
    }
}

const person = new Person();
person.printMyName();
person.printGender();
```

:large_blue_diamond:**(Spread & Rest) Operators**:large_blue_diamond:<br>
- Spread Default : 배열, 객체
```
const oldArray = [1,2,3]
const newArray = [...oldArray, 4]
```

- Rest Default : 함수
```
function sortArgs(...args){
    return args.sort()
}
```

:large_blue_diamond:**Destructuring (구조분할)**:large_blue_diamond:<br>
- Default
```
[a, b] = ['hi', 'hello']
```

:large_blue_diamond:**얕은복사 & 깊은복사**:large_blue_diamond:<br>
- 얕은복사 (참조복사, 객체복사)<br>
```
const a = [1,2,3]
const b = a // 참조복사
const c = {...a} // 객체복사
```

- 깊은복사<br>
 - 객체단위가 아닌 property까지 데이터를 가져와 새로 전부 만들어줘야함.<br>