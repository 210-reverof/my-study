(전체적으로 풀이에 어려움을 겪음)

# 1

```java
// 비트 연산이 익숙하지 않아서 
for(int i=0; i < ip.length;i++) {
	newAddress[i] = (byte)(ip[i] & subnet[i]);
	System.out.print(newAddress[i] >=0 ?
	newAddress[i] : newAddress[i]+256);
	System.out.print(".");
}
System.out.println();

for(int i=0; i < ip.length;i++) {
	hostAddress[i] = (byte)(ip[i] & ~subnet[i]);
	System.out.print(hostAddress[i] >=0 ?
	hostAddress[i] : hostAddress[i]+256);
	System.out.print(".");
}
System.out.println();
```

# 2

c

# 3

```java
url = new URL(address);
input = new BufferedReader(new InputStreamReader(url.openStream(), "UTF-8"));
while((line=input.readLine()) !=null) {
	ta.append(line);
	ta.append("\n");
}
```

# 4

```java
serverSocket = new ServerSocket(7777);
ta.setText(" .");
socket = serverSocket.accept();
ta.append("\r\n" +" .");
in = new DataInputStream(socket.getInputStream());
out = new DataOutputStream(socket.getOutputStream());
while(in!=null) {
	try {
		String msg = in.readUTF();
		ta.append("\r\n" + msg);
	} catch(IOException e) {}
}
```
