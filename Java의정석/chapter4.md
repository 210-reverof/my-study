# ch4

# 1

1. x > 10 && x < 20
2. ch != ‘ ‘ && ch ! = ‘\t’  (탭 표현 방법 몰랐음)
3. ch == ‘x’ && ch == ‘X’
4. ch  >= ‘0’ && ch <= ‘9’
5. ch >= ‘A’ && ch <=  ‘z’ 
6. year % 400 == 0 || year % 4 == 0 && year % 100 != 0
7. !powerOn
8. str.equals(”yes”)

# 2

73

```java
public class Main {
    public static void main(String[] args) {

        int answer = 0;
        for (int i = 1; i <= 20; i++) {
            if ( i%2 != 0 && i%3 != 0 ) answer+=i;
        }

        System.out.println(answer);    // 73
    }
}
```

# 3

220

```java
public class Main {
    public static void main(String[] args) {

        int answer = 0;
        int currentSum = 0;

        for (int i = 1; i <= 10; i++) {
            currentSum += i;
            answer += currentSum;
        }

        System.out.println(answer);   // 220
    }
}
```

# 4

199

```java
public class Main {
    public static void main(String[] args) {
        int sum = 0;
        int sign = -1;

        int i = 1;
        for (i = 1; sum < 100; i++) {
            sign *= -1;
            sum += sign * i;
            if (sum >= 100) break;
        }

        System.out.println(i + " ");
    }
}
```

# 5

```java
public class Main {
    public static void main(String[] args) {
        int i = 0;
        while (i <= 10) {
            int j = 0;
            while (j <= i) {
                System.out.println("*");
                j++;
            }
            System.out.println();
            i++;
        }
    }
}
```

# 6

```java
public class Main {
    public static void main(String[] args) {
        for (int i = 1; i < 6; i++) {
            for (int j = 0; j < 6; j++) {
                int sum = i+j;
                if (sum == 6) {
                    System.out.println(i + "+" + j + "=" + sum);
                }
            }
        }
    }
}
```

# 7

```java
(int) ( Math.random() * 6 ) + 1
```

# 8

```java
public class Main {
    public static void main(String[] args) {
        for (int i = 0; i <= 10; i++) {
            for (int j = 0; j <= 10; j++) {
                if (i * 2 + 4 * j == 10) {
                    System.out.println("x=" + i + ", y=" + j);
                }
            }
        }
    }
}

/*
x=1, y=2
x=3, y=1
x=5, y=0
*/
```

# 9

```java
sum += str.charAt(i) - ‘0’;
```

# 10

```java
while (num > 0) {
	sum += num % 10;
	num /= 10;
}
```

# 11

```java
num3 = num1 + num2;

num1 = num2;
num2 = num3;
```

# 12

```java
public class Main {
    public static void main(String[] args) {
        for (int i = 2; i <= 7; i++) {
            for (int j = 1; j <= 3; j++) {
                System.out.println(i + "*" + j + "=" + (i*j));
            }
            System.out.println("");
        }
    }
}
```

# 13

```java
ch = value.charAt(i);

if (ch < '0' || ch > '9') {
	isNumber = false;
	break;
}
```

# 14

```java
public class Main {
    public static void main(String[] args) {
        int answer = (int) (Math.random() * 100) + 1;   // (1)
        int input = 2;  // user's input
        int count = 0;
        
        do {
            count++;
            System.out.println("1가 100 사이의 값을 입력하세요 : ");
            input = 2; // scanner x
            
            // (2)
            if (answer > input) {
                System.out.println("더 큰 수를 입력하세요");
            } else if (answer < input) {
                System.out.println("더 작은 수를 입력하세요");
            } else {
                System.out.println("맞췄습니다.");
                System.out.println("시도횟수는 " + count + "번 입니다.");
                break;
            }
        } while (true);
    }
}
```

# 15
```java
result = (tmp % 10) + (result * 10);
tmp /= 10;
```
