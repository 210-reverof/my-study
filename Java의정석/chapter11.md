# 1

```java
kyo.addAll(list1);
kyo.retainAll(list2);
cha.addAll(list1);
cha.removeAll(list2);
hap.addAll(list1);
hap.removeAll(kyo);
hap.addAll(list2);
```

# 2

7

6

3

2

# 3

a - 첫번째를 제외한 모든 원소에 대해 작업 실행

# 4

// 5번째 요소 (오답?)

6번째 : 제일 가운데 요소

 

# 5

```java
public int compareTo(Object o) {
	if(o instanceof Student) {
		Student student = (Student)o;
		return name.compareTo(student.name)
	} else {
		return -1;
	}
}
```

# 6

```java
static int getGroupCount(TreeSet tset, int from, int to) {
	Student s1 = new Student("", 0, 0, from, from, from);
	Student s2 = new Student("", 0, 0, to, to, to);
	return tset.subSet(s1,s2).size();
}
```

# 7

```java
public int compare(Object o1, Object o2) {
	if(o1 instanceof Student && o2 instanceof Student) {
		Student s1 = (Student)o1;
		Student s2 = (Student)o2;
		int result = s1.ban - s2.ban;
		if(result==0) { // , . 반이 같으면 번호를 비교한다
			return s1.no - s2.no;
		}
		return result;
	}
	return -1;
}
```

# 8

```java
for(int i=0;i < length; i++) {
	Student s = (Student)list.get(i);
	if(s.total==prevTotal) {
		s.schoolRank = prevRank;
	} else {
		s.schoolRank = i + 1;
	}
	prevRank = s.schoolRank;
	prevTotal = s.total;
}
```

# 9

```java
Student s1 = (Student)o1;
Student s2 = (Student)o2;
int result = s1.ban - s2.ban;
if(result==0)
result = s2.total - s1.total;
return result;
```

```java
for(int i=0, n=0; i < length; i++, n++) {
	Student s = (Student)list.get(i);
	if(s.ban!=prevBan) {
		prevRank = -1;
		prevTotal = -1;
		n = 0;
	}
	if(s.total==prevTotal) {
		s.classRank = prevRank;
	} else {
		s.classRank = n + 1;
	}
	prevBan = s.ban;
	prevRank = s.classRank;
	prevTotal = s.total;
}
```

# 10

HashSet을 순서를 보장하지 않기 때문에 순서 보장 ArrayList 혹은 LinkedList를 활용한다

# 11

```java
public int hashCode() {
	return toString().hashCode();
}
```

# 12

```java
if(c1.isKwang && c2.isKwang) {
	result = (Integer)jokbo.get("KK");
} else {
	result = (Integer)jokbo.get(""+c1.num+c2.num);
	if(result==null) {
		result = new Integer((c1.num + c2.num) % 10 + 1000);
	}
}
p.point = result.intValue();
```

# 13

```java
if(o1 instanceof Player && o2 instanceof Player) {
	Player p1 = (Player)o1;
	Player p2 = (Player)o2;
	return p2.point - p1.point;
}
return -1;
```

# 14

```java
do {
	try {
		menu = Integer.parseInt(s.nextLine().trim());
		if(1 <= menu && menu <= 3) {
			break;
		} else {
		throw new Exception();
		}
	} catch(Exception e) {
		System.out.println(" . .");
		System.out.print(" .(1~3) : ");
	}
} while(true);
```
