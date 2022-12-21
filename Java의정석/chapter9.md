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

# 7

```java
public static boolean contains(String src, String target) {
	return src.indexOf(target)!=-1;
}
```

# 8

```java
public static double round(double d, int n) {
	return Math.round(d * Math.pow(10, n)) / Math.pow(10,n);
}
```

# 9

```java
public static String delChar(String src, String delCh) {
String str = str;

for(int i=0; i < src.length();i++) {
	char ch = src.charAt(i);
	if(delCh.indexOf(ch)==-1)
		str += ch;
}
		return str
}
```

# 10

```java
static String format(String str, int length, int alignment) {
	int diff = length - str.length();
	if(diff < 0) return str.substring(0, length);
	char[] source = str.toCharArray();
	char[] result = new char[length];
	
	for(int i=0; i < result.length; i++)
		result[i] = ' ';
	
	switch(alignment) {
		case 0 :
		default :
			System.arraycopy(source, 0, result, 0, source.length);
		break;
		case 1 :
			System.arraycopy(source, 0, result, diff/2, source.length);
		break;
		case 2 :
			System.arraycopy(source, 0, result, diff, source.length);
		break;
	}
	return new String(result);
}
```

# 11

```java

```

# 12

```java
public static int getRand(int from, int to) {
	return (int)(Math.random() * (Math.abs(to-from)+1))+ Math.min(from,to);
}
```
