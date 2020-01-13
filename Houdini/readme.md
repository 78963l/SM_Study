# Houdini
## [(main)](/readme.md) 
* * *
### create
* * *
- cube 생성  
Geo = hou.node('obj/').createNode("geo")  
Box = Geo.createNode('box')  
Box.setDisplayFlag(True)  