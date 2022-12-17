# 1

```java
for (int i = 0; i < CARD_NUM / 2; i++) {
	if (i == 1 || i == 3 || i == 8) {
		cards[i] = new SutdaCard(i ,true);
	} else {
		cards[i] = new SutdaCard(i, false);
	}

	cards[i + (CARD_NUM / 2)] = new SutdaCard(i, false);
}
```

# 2

```java
void shuffle() {
	for (int i = 0; i < CARD_NUM; i++) {
		int pos = (int) Math.random() * CARD_NUM;
		SutdaCard temp = cards[pos];
		cards[pos] = cards[i];
		cards[i] = cards[pos];
	}
}

SutdaCard pick(int index) {
	if(index < 0 || index >= CARD_NUM) return null
	return cards[index]; 
}

SutdaCard pick() {
	int pos = (int) Math.random() * CARD_NUM;
	return cards[pos];
}
```

# 3

```java
//오버라이딩의 정의
```

# 4

```java
c. 좁거나 같아야함
b. 조상 메소드보다 더 적은 수의 예외
```

# 5

```java
부모 클래스 생성자가 파라미터가 필요한 생성자만 존재한다.
따라서 현재 코드의 자식 클래스는 부모 클래스를 초기화 하지 않는다.

Product 클래스 내부에 Product(){} 생성
```

# 6

```java
// 
```

# 7

```java
//생성자 호출 순서
Parent() -> Child()

//출력 결과
200
```

# 8

```java
a
```

# 9

```java
b - 상속이 불가능하다.
```
