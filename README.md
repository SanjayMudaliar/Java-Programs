# Java Numbers Program.


### Program 1

WJP to print assci values of the given character.

```java
        char ch = 'A';
		int a = ch;
		System.out.println(a);
```

Another Way using Methods..

```java
    public class AsciiValue {

	    static int ascii(char c) {
		
		int as = c;
		
		return c;//we can return value directly as (return c)
	}

	public static void main(String[] args) {
		
		Scanner sc = new Scanner(System.in);
		
		System.out.println("enter the character");
		char ch = sc.next().charAt(0);
		
		int num = ascii(ch);
		
		System.out.println("Ascii value of "+ch+" is "+num);
```

### Program 2

WJP to check wheather given char is vowel or not using Switch Case.

```java
public class CheckVowels {

	public static void main(String[] args) {
		
		Scanner sc = new Scanner(System.in);
		
		System.out.println("enter the char");
		char c = sc.next().charAt(0);
		
		
		switch(c) {
		
		//We can pass the multiple values in case..
		
		case 'A' , 'a' : System.out.println("vowel");
		break;
		
		case 'e', 'E' : System.out.println("vowel");
		break;
		
		case 'i', 'I' : System.out.println("vowel");
		break;
		
		case 'o', 'O' : System.out.println("vowel");
		break;
		
		case 'u', 'U' : System.out.println("vowel");
		break;
		
		default : System.out.println("not vowel");
		}	
	}
```

### Program 3

WJP to check wheather given number is composite or not.

```java
    int num = 17;
		int flag = 0;
		
		for(int i=2; i<=num/2; i++) {
			
			if(num % i == 0) {
				flag = 1;
				System.out.println("Composite number");
				break;
			}
		}
		
		if(flag == 0) {
			System.out.println("not composite number");
		}
```

### Program 4

WJP to print composite number in the  given range.

```java
	int num = 12;
		
		for(int i=2; i<=num; i++) {
			int flag = 0;

			for(int j=2; j<=i/2; j++) {
				
				if(i%j==0) {
					flag = 1;
				}
			}
			
			if(flag == 1) {
				System.out.println(i);
			}
		}
```

### Program 5

WJP to count no. of digit in given number.

```java
		int num = 12345;
		
		int count = 0;
		
		while(num != 0) {
			
			num/=10;
			count++;
		}
		
		System.out.println("Total digits is "+count);
	}
```

### Program 6


WJP for check the number even or odd without using the % operator.

>Hint : number/2*2 == number

```java
	int a = 50;
		
		if(a/2*2 == a) {
			System.out.println("Even");
		}
		else {
			System.out.println("odd");
		
	}
```

### Program 7

WJP to check wheather the first digit of number is even or odd.

```java
		int num = 2234;
		
		//number should be greater than 9
		while(num > 9) {
			
			num/=10;
			
		}
		
		if(num%2==0) {
			System.out.println("even");
		}
		else {
			System.out.println("odd");
		}
	}
```

### Program 8

WJP to find the Factorial of the given number.

```java
		int num = 3;
		int fac = 1;
		
		//5! = 5*4*3*2*1

		for(int i=1; i<=num; i++) {
			
			fac*=i;
		}
		
		System.out.println(fac);
	}
```

### Program 9

WJP to find the Factors of the given number.

```java
		int num = 16;
		
		for(int i=1; i<=num; i++) {
			
			if(num % i == 0) {
				System.out.print(i+" ");
			}
			
		}
```

### Program 10

WJP to check wheather given data is alphabet or number
or special char.

```java
		char c = '@';
		
		if('a'<=c && c<='z' || 'A'<=c && c<='Z') {
			System.out.println("data is char");
		}
		
		else if('0'<=c && '9'>=c) {
			System.out.println("data is number");
		}
		
		else {
			System.out.println("data is special char");
		}
```

### Program 11

WJP to find largest number from three number using contional operator.

>Ternary Operator :
>(condition) ? true : false;

```java
	int a = 40, b= 20, c=30;
	
	//Ternary Oparator returns the values.

	int res = (a>b)? (a>c)?a:c : (b>c)? b:c;

	System.out.println(res);
```
Without using Operator.

```java
	int a = 40, b= 20, c=30;

	if(a>b){
		if(a>c){
			System.out.println(a);
		}
		else{
			System.out.println(c);
		}
	}
	else if(b>c){
		System.out.println(b);
	}
	else{
		System.out.println(c);
	}
```

### Program 12

WJP to find wheather the given is palindrome or not.

```java
		int num = 123212, rev = num;
		int res = 0;
		
		while(num != 0) {
			
			int last = num % 10;
			res = (res*10) + last;
			num/=10;
			
		}
		
		if(rev == res) {
			System.out.println("palindrome");
		}
		else {
			System.out.println("Not a palindrome");
		}
```

### Program 13

WJP to check a given number is perfect number or not.

>Perfect number is the number in which the sum of factors of that number execpt that number is equals to that number.

>For example : 1+2+3 = 6

```java
		int num = 6;
		int sum = 0;
		
		for(int i=1; i<num; i++) {
			
			if(num % i == 0) {
				sum+=i;
			}
		}
		
		if(sum == num) {
			System.out.println("Perfect Number");
			System.out.println("original number is "+num);
			System.out.println("sum is "+sum);
		}
		else {
			System.out.println("Not Perfect Number");
			System.out.println("original number is "+num);
			System.out.println("sum is "+sum);
		}
```

### Program 14

WJP to check the given number is Prime Number or not.

```java
		int num = 29;
		boolean b = true;
		
		//factors of the number will be exactly upto half of
		//the main number
		
		for(int i=2; i<=num/2; i++) {
			
			if(num % i == 0) {
				b = false;
				System.out.println("number is not prime");
				break;
			}
		}
		
		if(b==true) {
		System.out.println("number is prime");
		}
```

### Program 15

WJP to print the Prime Number till the given Number..

```java
		int num = 100;
		
		//for the range
		for(int i=2; i<=100; i++) {
			
			int flag = 0;

			//for the prime number
			for(int j=2; j<=i/2; j++) {
				
				if(i%j==0) {
					flag = 1;
				}
			}
			
			if(flag == 0) {
				System.out.println(i);
			}
		}
```

### Program 16

WJP to find the product of the given number using digits present in the Number..

```java
		int num = 555;
		int last , res =1;
		
		while(num != 0) {
			
			last = num % 10;
			res *= last;
			num/=10;
		}
		
		System.out.println(res);
```

### Program 17

WJP to reverse the given Number.

```java
		int num = 123454;
		int res = 0, last = 0;
		
		while(num > 0) {
			
			last = num % 10;
			
			res = (res * 10) + last;
			
			num/=10;
			
		}
		
		System.out.println(res);
```

### Program 18

WJP to find the Sum of the number using digits.

```java
		int num = 123;
		int last , res =0;
		
		while(num != 0) {
			
			last = num % 10;
			res += last;
			num/=10;
		}
		
		System.out.println(res);
```

### Program 19

WJP to find sum of the factors of the given Number.

```java
		int num = 6;
		int sum=0;
		
		for(int i=1; i<=num; i++) {
			
			if(num % i == 0) {
				sum+=i;
			}	
		}
		
		System.out.println(sum);
```

### Progam 20

Explanation about the next() and nextLine() in Scanner Class.

```java
		Scanner sc = new Scanner(System.in);
		
		System.out.println("read the data for next");
		//Hello I am here
		String s1 = sc.next();//Hello
		
		//I am here
		System.out.println(sc.nextLine());
		
		System.out.println("read the data for nextLine");
		//YooBoy
		String s2 = sc.nextLine();
		
		System.out.println(s1);//Hello
		System.out.println(s2);//YooBoy
```



