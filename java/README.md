
# 練習網址 mgiga.com.tw
# 考試 w9.mgiga.com.tw


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

## BMI

```
package test;
import java.text.DecimalFormat;
import java.text.Format;
import java.util.Scanner;
public class test0518 {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
    Scanner input = new Scanner(System.in);
    System.out.println("請輸入身高");
    double cm = input.nextDouble();
    System.out.println("請輸入體重");
    double kg = input.nextDouble();
    double m = cm*0.01;
    double bmi = kg / (m*m);
    
    
    Format fm = new DecimalFormat("##0.0");
    System.out.print("您的BMI為:");
    System.out.println(fm.format(bmi));
	
	if(bmi<18){
    	System.out.println("過輕");
    } else if(bmi<25){
    	System.out.println("剛好");
    } else if(bmi<30){
    	System.out.println("過重");
    } else {
    	System.out.println("超重");
    }
    
 }
}

```
<img src="https://github.com/4060E006/homework/blob/master/picture/java0518.jpg" width="80%" height="80%">


#### round = 四捨五入
#### floor = 無條件捨去
#### ceil = 無條件進位

```
public static void main(String[] args) {
		
        
		String aa = "1.6";
		String bb = "2.7";
		double aa0 = Double.parseDouble(aa);
		double bb0 = Double.parseDouble(bb);
		
		int aa2 = (int) Math.round(aa0);
		int bb2 = (int) Math.round(aa0);
				
	
		System.out.println((aa2+bb2));
	}

}
```
## 小數判斷

```
Scanner input = new Scanner(System.in);
		double a = input.nextDouble();	
		
	       if(a%2==0||a%2==1){
	        System.out.println("int");
	       }else{
	        System.out.println("double");
	       }
```

## 捨棄小數點前面的值
```
String A = input.next();
A = A.replace("."," ");

String []B = A.split(" ");
int C = Integer.parseInt(B[1]);

System.out.println(C)
```

## 取到小數第二位
```
String a1 = "1.54684";
Double a = Double.paresDouble(s1);
B = (double) Math.round((B*100))/100;
```
```
可輸入學生的數學與英文成績(0~100整數)，將數學乘以0.65，將英文乘以0.35，’ 相加後印出結果
(四捨五入到小數以下 1 位)。
範例如下:
(1) 使用者輸入 10 20
    則程式印出 13.5
(2) 使用者輸入 17 38
    則程式印出 24.4
註: 主程式類別名稱請使用 MainClass。

import java.util.Scanner;
import java.text.Format;
import java.text.DecimalFormat;

public class MainClass{
public static void main(String[] args){

Scanner input = new Scanner(System.in);
int num1 = input.nextInt();
int num2 = input.nextInt();
double num3 = num1*0.65;
double num4 = num2*0.35;
double num5 = num3+num4;

Format fm = new DecimalFormat("##0.0");
System.out.println(fm.format(num5));
}
}
```
```
請寫程式，可輸入包含空白的整數或小數，程式可以將這個數字加上 2 後印出?
(四捨五入到小數以下 1 位)。
範例如下:
(1) 使用者輸入 10      
    則程式印出 12.0
(2) 使用者輸入      1.556
    則程式印出 3.6
註: 主程式類別名稱請使用 MainClass。

import java.util.Scanner;
import java.text.Format;
import java.text.DecimalFormat;

public class MainClass{
public static void main(String[] args){

Scanner input = new Scanner(System.in);
String num1 = input.nextLine();
double num2 = Double.parseDouble(num1);
double num3 = num2 + 2.0;

Format fm = new DecimalFormat("##0.0");
System.out.println(fm.format(num3));

}
}

```
```
請寫一個程式，可輸入兩個數(整數或小數)與一個運算符號(+, -, *. /)，中間用空白隔開，程式可以將這兩個數字依照運算符號計算，並印出結果(四捨五入到小數以下一位)?
範例如下:
(1) 使用者輸入 10 + 20
    則程式印出 30.0
(2) 使用者輸入 1.55 * 2.13
    則程式印出 3.3
註: 主程式類別名稱請使用 MainClass。

import java.util.Scanner;
import java.text.Format;
import java.text.DecimalFormat;

public class MainClass{
public static void main(String[] args){

Scanner input = new Scanner(System.in);
String num = input.nextLine();
String []str1 = num.split(" ");
double num1 = Double.parseDouble(str1[0]);
double num2 = Double.parseDouble(str1[2]);
double num3 = 0;

if(str1[1].equals("+")) num3 = (double)num1+num2;
if(str1[1].equals("-")) num3 = (double)num1-num2;
if(str1[1].equals("*")) num3 = (double)num1*num2;
if(str1[1].equals("/")) num3 = (double)num1/num2;

Format fm = new DecimalFormat("##0.0");
System.out.println(fm.format(num3));
 
}
}
```
```
程式可輸入一串英數字，中間可能會有空白，程式可以空白去除，並將所有 AB 替換成 12，再印出結果
範例如下:
(1) 使用者輸入 34R  ABTYAB10
    則程式印出 34R12TY1210
(2) 使用者輸入 A9B5CD
    則程式印出 A9B5CD
註: 主程式類別名稱請使用 MainClass。
import java.util.Scanner;
public class MainClass{
public static void main(String[] args){

Scanner input = new Scanner(System.in);
String num1 = input.nextLine();
num1 = num1.replaceAll("AB","12");
num1 = num1.replaceAll(" ","");
System.out.println(num1);

}
}
```
```
程式可輸入學生的成績(0~100整數)，並將上述成績乘以0.125，並印出結果
(四捨五入到小數以下2位)。
範例如下:
(1) 使用者輸入 7
    則程式印出 0.88
(2) 使用者輸入 13
    則程式印出 1.63
註: 主程式類別名稱請使用 MainClass。
import java.util.Scanner;
import java.text.Format;
import java.text.DecimalFormat;

public class MainClass{
public static void main(String[] args){
Scanner input = new Scanner(System.in);
int num = input.nextInt();
double num1 = num * 0.125;
Format fm = new DecimalFormat("##0.00");
System.out.println(fm.format(num1));

}
}
```



