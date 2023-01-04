# 1

```java
(String name, int i) -> { System.out.println(name+"="+i); }

(name, i) -> { System.out.println(name+"="+i); }

(name, i) -> System.out.println(name+"="+i)
```

```java
(int x) -> x * x

(x) -> x * x

x -> x * x
```

```java
() -> { return (int)(Math.random()*6); }

() -> (int)(Math.random() * 6)
```

```java
(int[] arr) -> {
	int sum = 0;
	for(int i : arr)
		sum += i;
	return sum;
}
```

```java
() -> new int[]{}
```

# 2

String :: length

int[] :: new

Arrays :: stream

String :: equals

Integer :: compare

Card :: new

System.out :: println

Math :: random

String :: toUpperCase

NullPointerException :: new

Optional :: get

StringBuffer : append

System.out :: println

# 3

d

# 4

```java
int sum = strStream.mapToInt(String::length).sum();
```

# 5

```java
strStream.map(String::length).sorted(Comparator.reverseOrder()).limit(1).forEach(System.out::println);
```

# 6

```java
new Random().ints(1,46).distinct().limit(6).sorted().forEach(System.out::println);
```

# 7

```java
die.flatMap(i-> Stream.of(1,2,3,4,5,6).map(i2 -> new int[]{ i, i2 })).filter(iArr-> iArr[0]+iArr[1]==6).forEach(iArr -> System.out.println(Arrays.toString(iArr)));
```

# 8

```java
Map<Boolean, Map<Boolean, Long>> failedStuBySex = Stream.of(stuArr).collect(partitioningBy(Student::isMale, partitioningBy(s -> s.getScore() < 150, counting())));
```
