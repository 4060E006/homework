```
練習網址 mgiga.com.tw
w9.mgiga.com.tw
```

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


