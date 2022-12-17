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

# 10

```java
public void setVolume(int volume) {
    if(volume > MAX_VOLUME || volume < MIN_VOLUME) return;
    this.volume = volume;
}
        
public int getVolume() {
    return volume;
}
        
public void setChannel(int channel) {
    if(channel > MAX_CHANNEL || channel < MIN_CHANNEL) return;
    this.channel = channel;
}
    
public int getChannel(){
   return channel;
}
```

# 11

```java
public void gotoPrevChannel() {
	setChannel(prevChannel);
}
```

# 12

c - 사용 불가능

# 13

// 몰랐었음

인스턴스 변수가 존재하지 않기 때문에 객체를 생성할 필요가 없음

# 14

```java
final int NUM;
final boolean IS_KWANG;
```

# 15

e - 하위클래스로 상위클래스가 형변환 불가

# 16

e

# 17

```java

```
