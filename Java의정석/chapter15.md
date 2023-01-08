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

# 3

```java
public static void countFiles(File dir) {
	File[] files = dir.listFiles();
	for(int i=0; i < files.length; i++) {
		if(files[i].isDirectory()) {
			totalDirs++;
			countFiles(files[i]);
		} else {
			totalFiles++;
			totalSize += files[i].length();
		}
	}
}
```

# 4

```java
public static void main(String[] args) {
	if(args.length < 2) {
		System.out.println("파일 이름");
		System.exit(0);
	}

	try {
		Vector v = new Vector();
		for(int i=1; i < args.length;i++) {
			File f = new File(args[i]);
			if(f.exists()) {
				v.add(new FileInputStream(args[i]));
			} else {
				System.out.println(args[i]+ " - .");
			}
		}
		SequenceInputStream input = new SequenceInputStream(v.elements());
		FileOutputStream output = new FileOutputStream(args[0]);
		int data = 0;
		while((data = input.read())!=-1) {
			output.write(data);
		}
	} catch(IOException e) {}
}
```

# 5

```java
public void write(int c) throws Exception {
	if(c=='<') {
		inTag = true;
	} else if(c=='>' && inTag) {
		inTag = false;
		tmp = new StringWriter();
		return;
	}
	if(inTag) tmp.write(c);
	else out.write(c);
}
```

# 6

```java
if("..".equals(subDir)) {
	File newDir = curDir.getParentFile();
	if(newDir==null) {
		System.out.println(" ."); 
	} else {
		curDir = newDir; 
	}
} else if(".".equals(subDir)) {
	System.out.println(curDir);
} else {
	File newDir = new File(curDir, subDir);
	if(newDir.exists() && newDir.isDirectory()) {
		curDir = newDir;
	} else {}
}
```
