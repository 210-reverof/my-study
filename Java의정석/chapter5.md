# 1

// a, 초기화 혹은 원소 할당을 안하였다. (오답)

- d : new int[] 로 크기를 지정했을 때는 대괄호로 크기를 지정할 수 없다.
- e : 선언할 때는 배열의 크기를 지정할 수는 없고, new int와 같이 할당하며 지정한다.

# 2

2

# 3

```java
for (int i = 0;i<arr.length;i++) {
	sum += arr[i];
}
```

# 4

```java
for (int i = 0; i < arr.length; i++) {
    for (int j = 0; j < arr[i].length; j++) {
        total += arr[i][j];
     }
}
average = (float)total / (float)arr.length;
```

# 5

```java
tmp = ballArr[i];
ballArr[i] = ballArr[j];
ballArr[j] = tmp;
```

# 6

```java
System.out.println(coinUnit[i] + "원: " + (money / coinUnit[i]));
money = money % coinUnit[i];
```

# 7

```java
// 1
coinNum = money / coinUnit[i];

// 2
if (coinNum <= coin[i]) coin[i] -= coinNum;
else {
	coinNum = coin[i];
	coin[i] = 0;
}

// 3
money -= coinNum * coinUnit[i];
```

# 8

```java
// 1
counter[answer[i] - 1]++;

// 2
System.out.print(counter[i]);

for (int j = 0; j < counter[i]; j++) {
	System.out.print("*");
}
```
