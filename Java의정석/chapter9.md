# 1

# 2

```java
if(ob instanceof Point3D) {
	Point3D p = (Point3D) ob;
	return x==p.x && y==p.y && z==p.z;
}
return false;
```

# 3

```java
int pos = fullPath.lastIndexOf("\\");
if(pos!=-1) {
	path = fullPath.substring(0, pos);
	fileName = fullPath.substring(pos+1);
}
```

# 4

```java
for(int i=0; i < dataArr.length;i++) {
	for(int j=0; j < dataArr[i];j++) {
		System.out.print(ch);
	}
	System.out.println(dataArr[i]);
}
```

# 5

```java
while(true) {
	pos = src.indexOf(target,pos);
	if(pos!=-1) {
		count++;
		pos += target.length();
	} else {
		break;
	}
}
```
