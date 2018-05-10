
###### constant = 常數
###### variable = 變數

#### toCharArray() = 將字串轉換成數字
```
String str1 = "1234";
char ch1[] = str1.toCharArray();
System.out.println(ch1);
```
#### 字串比對
```
Scanner input = new Scanner(System.in); 
		 String num = input.nextLine();
		 String comp = "";
		 
		 if (num.equals("c8763")) comp = "噓";
		 else comp = "錯誤";
		 System.out.println(comp); 
```
#### 字串拆解

##### 拆解後需要用陣列來儲存
##### 如果需要轉成整數，則用 Integer.parseInt()
##### 如果需要轉成小數，則用 Integer.parseDouble() 
```
System.out.println("輸入的字中間加上空白將會補上逗號");
		 Scanner input = new Scanner(System.in);
		 String number = input.nextLine();
		 String []str1 = number.split(" "); // 依照空白拆解成陣列
		 System.out.println(str1[0]+","+str1[1]);
		 
System.out.println("輸入的數字中間加上空白將會將兩數相乘");
		 Scanner input = new Scanner(System.in);
		 String number = input.nextLine();
		 String []str1 = number.split(" "); // 依照空白拆解成陣列
		 int num1 = Integer.parseInt(str1[0]);
		 int num2 = Integer.parseInt(str1[1]);
		 int num3 = num1*num2; 
		 System.out.println(num3);
		 
System.out.println("兩數中間空白加上運算符號即可以運算");		 
		 Scanner input = new Scanner(System.in);
		  String value = input.nextLine();
		  String []str1 = value.split(" ");
		  int v1 = Integer.parseInt(str1[0]); // 6
		  int v2 = Integer.parseInt(str1[2]); // 5
		  double v3 = 0;
		  if (str1[1].equals("+")) v3 = v1+v2;
		  if (str1[1].equals("-")) v3 = v1-v2;
		  if (str1[1].equals("*")) v3 = v1*v2;
		  if (str1[1].equals("/")) v3 =(double) v1/v2;
		  Format fm = new DecimalFormat("##0.00");
		  System.out.println(fm.format(v3)); 
``` 
