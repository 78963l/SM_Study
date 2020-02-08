# Maya
※ 마야는 기본적으로 C/C++ 언어로 만들어져 있고, Maya의 모든 GUI와 command가 MEL로 만들어져 있다.
※ 마야는 (DG(Dependency Graph)-수평(Hypergraph InputOutput)), (DAG(Directed Acyclic Graph)-수직(Outliner)) 구조로 연결된 노드의 구성으로 만들어져 있다.
### [(main)](/readme.md) 
* * *
### 기능
:large_blue_diamond:**attribute 확인**:large_blue_diamond:  
- import maya.cmds as cmds  
for x in cmds.listAttr("Sphere1"):print x   

### create
* * *
- cube 생성  
cmds.polyCube(n='Cube')

