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
