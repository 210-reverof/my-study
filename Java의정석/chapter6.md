# 1

```java
class SutdaCard {
	int num;
	boolean isKwang;
}
```

# 2

```java
class SutdaCard {
	int num = 1;
    boolean isKwang = true;
    
    SutdaCard(int num, boolean isKwang) {
        this.num = num;
        this.isKwang = isKwang;
    }

    SutdaCard() {
    }

    String info() {
        String info = num + "";
        if (isKwang) info += "K";
        return info;
    }
}
```

# 3

```java
class Student {
	String name;
	int ban;
	int no;
	int kor;
	int eng;
	int math;
}
```

# 4

```java
class Student {
	String name;
	int ban;
	int no;
	int kor;
	int eng;
	int math;
	
	int getTotal() {
		return kor + eng + math;
	}

	float getAverage() {
		return (float) (getTotal() / 3f * 10 + 0.5f) / 10f;
	}
}

```

# 5

```java
class Student {
	String name;
	int ban;
	int no;
	int kor;
	int eng;
	int math;
	
	int getTotal() {
		return kor + eng + math;
	}

	float getAverage() {
		return (float) (getTotal() / 3f * 10 + 0.5f) / 10f;
	}

	public String info() {
		return name +","+ ban +","+ no +","+ kor
					+","+eng +","+ math +","+getTotal() +","+getAverage();
	}
}

```

# 6

```java
return Math.sqrt((x - x1) * (x - x1) + (y - y1)*(y - y1));
```

# 7

```java
double getDistance(int x1, int y1) {
	return Math.sqrt((x - x1) * (x - x1) + (y - y1) * (y - y1));
}
```

# 8

- local : k, n, card, args
- instance : kind, num
- class : width, height

# 9

weapon, armor - Marine . 모든 인스턴스에 대해 동일한 값이어야 하므로
weaponUp(), armorUp() - static변수에 대한 작업을 하는 메서드이므로

# 10

b : 초기화를 위해

e : 여러 개의 생성자 생성 가능

# 11

b : 클래스에서는 static 불가

# 12

c : 오버로딩과 관련 x

d : 오버로딩과 관련 x

# 13

b, c, d

# 14

c, e

# 15

a

# 16

a, e

# 17

// b, c : 오답

b

# 18

// A, B : 오답

A, B, D

# 19

ABC123

After change : ABC123

# 20

```java
public static int[] shuffle(int[] arr) {
	for(int i = 0; i < arr.length;i++) {
		int j = (int) (Math.random() * arr.length);
		int tmp = arr[i];
		arr[i] = arr[j];
		arr[j] = tmp;
	}

	return arr;
}
```
