# 1

```java
Calendar cal = Calendar.getInstance();
        cal.set(2010, 0, 1);
        for (int i = 0; i < 12; i++) {
            int weekday = cal.get(Calendar.DAY_OF_WEEK)
            int secondSunday = (weekday == 1) ? 8 : 16 - weekday;
            cal.set(Calendar.DAY_OF_MONTH, secondSunday);
            Date d = cal.getTime();
            System.out.println(new SimpleDateFormat("yyyy-MM-dd F E 은 번째 요일입니다.").format(d));
            
            cal.add(Calendar.MONTH, 1);
            cal.set(Calendar.DAY_OF_MONTH, 1);
        }
```

# 2

```java
static int paycheckCount(Calendar from, Calendar to) {
        if (from == null || to == null)
            return 0;
        if (from.equals(to) && from.get(Calendar.DAY_OF_MONTH) == 21) {
            return 1;
        }
        int startYear = from.get(Calendar.YEAR);
        int startMon = from.get(Calendar.MONTH);
        int startDay = from.get(Calendar.DAY_OF_MONTH);
        int endYear = to.get(Calendar.YEAR);
        int endMon = to.get(Calendar.MONTH);
        int endDay = to.get(Calendar.DAY_OF_MONTH);
    
        int monDis = (endYear * 12 + endMon) - (startYear * 12 + startMon);
        
        if (monDis < 0)
            return 0;

        if (startDay <= 21 && endDay >= 21)
            monDis++;

        if (startDay > 21 && endDay < 21)
            monDis--;
        return monDis;
    }
```

# 3

```java
String data = "123,456,789.5";
DecimalFormat df = new DecimalFormat("#,###.##");
DecimalFormat df2 = new DecimalFormat("#,####");
            
Number num = df.parse(data);
double d = num.doubleValue();
System.out.println("data:"+data);
System.out.println(" :"+Math.round(d));
System.out.println(" :"+df2.format(d));
```

# 4

```java
public static void main(String[] args) {
String pattern = "yyyy/MM/dd";
String pattern2 = " E .";
DateFormat df = new SimpleDateFormat(pattern);
DateFormat df2 = new SimpleDateFormat(pattern2);
Scanner s = new Scanner(System.in);
Date inDate = null;
do {
System.out.println(" " + pattern 날짜를
+ " .( :2007/05/11)"); 의 형태로 입력해주세요 입력예
try {
System.out.print(">>");
inDate = df.parse(s.nextLine()); // Date . 입력받은 날짜를 로 변환한다
break; // parse() . 에서 예외가 발생하면 이 문장은 수행되지 않는다
} catch(Exception e) {}
} while(true);
System.out.println(df2.format(inDate));
} // main
```

# 5

```java
public static void main(String[] args) {
        String pattern = "yyyy/MM/dd";
        String pattern2 = " E .";
        DateFormat df = new SimpleDateFormat(pattern);
        DateFormat df2 = new SimpleDateFormat(pattern2);
        Scanner s = new Scanner(System.in);

        Date inDate = null;
        do {
            System.out.println(" " + pattern + " .( :2007/05/11)");
            try {
                System.out.print(">>");
                inDate = df.parse(s.nextLine());
                break;
            } catch (Exception e) {
            }
        } while (true);
        System.out.println(df2.format(inDate));
    }
```
