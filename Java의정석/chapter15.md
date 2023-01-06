# 1

```java
try {
	int lineNum = Integer.parseInt(args[0]);
	String fileName = args[1];
	File f = new File(fileName);
            
	if (f.exists() && !f.isDirectory()) {
		BufferedReader br = new BufferedReader(new FileReader(fileName));
		String line = "";
    int i = 1;
    
		while ((line = br.readLine()) != null && i <= lineNum) {
			System.out.println(i + ":" + line);
      i++;
	   }
   } else {
	   throw new FileNotFoundException(fileName + ".");
   }
  } catch (Exception e) {
  }
```

# 2

```java
if (args.length != 1) {
            System.out.println("USAGE: java HexaViewer FILENAME");
            System.exit(0);
        }
        String inputFile = args[0];
        try {
            FileInputStream input = new FileInputStream(inputFile);
            PrintStream output = new PrintStream(System.out);
            int data = 0;
            int i = 0;
            while ((data = input.read()) != -1) {
                output.printf("%02X ", data);
                if (++i % 16 == 0)
                    output.println();
            }
            input.close();
            output.close();
        } catch (Exception e) {

        }
```
