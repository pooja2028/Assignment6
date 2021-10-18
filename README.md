# Assignment6
 Binary.java 
@@ -0,0 +1,24 @@
import java.util.Scanner;
public class  Binary
{
    public static void main(String[] args) 
    {
        int n, count = 0, a;
        String x = "";
        Scanner s = new Scanner(System.in);
        System.out.print("Enter any decimal number:");
        n = s.nextInt();
        while(n > 0)
        {
            a = n % 2;
            if(a == 1)
            {
                count++;
            }
            x = a + "" + x;
            n = n / 2;
        }
        System.out.println("Binary number:"+x);

    }
}


 BIN +1.31 KB CouponNumber.class 
Binary file not shown.
 20  CouponNumber.java 
@@ -0,0 +1,20 @@
public class CouponNumber
{
	public static void main(String[] args)
	{
		char[] chars="abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ123456789".toCharArray();
		int max=100000000;
		int random=(int) (Math.random()*max);
		 StringBuffer sb=new StringBuffer();


		while (random>0)
		{
			sb.append(chars[random % chars.length]);
			random /= chars.length;
		}

		String couponCode=sb.toString();
		System.out.println("Coupon Code: "+couponCode);	
	}
}


 BIN +1.35 KB DayofWeek.class 
Binary file not shown.
 76  DayofWeek.java 
@@ -0,0 +1,76 @@
import java.util.Scanner;

 public class DayofWeek {
   public static void main(String[] args) {

     Scanner scanner = new Scanner(System.in);

     boolean keepGoing = true;

     while(keepGoing) {
       System.out.println("Month");
       int m = scanner.nextInt();
         if (m < 1 || m > 12) {
           System.out.println("Months are between 1 and 12");
           continue;
         }

       System.out.println("Day");
       int d = scanner.nextInt();
         if (d < 1 || d > 31) {
            System.out.println("Days are between 1 and 31");
            continue;
         }

       System.out.println("Year");
       int y = scanner.nextInt();
         if (y < -10000 || y > 10000) {
            System.out.println("Years are between -10000 and 10000");
            continue;
         }

        int y0 = y - (14 - m) / 12;
        int x = y0 + y0/4 - y0/100 +y0/400;
        int m0 = m + 12 * ((14 - m) / 12) - 2;
        int d0 = (d + x + 31 * m0 / 12) % 7;  
        boolean c = 0 <= d0 && d0 <= 6;
	switch(day)
	{
		case 0:
			System.out.println("Sunday");
			break;
		case 1:
                        System.out.println("Monday");
                        break;

		case 2:
                        System.out.println("Tuesday");
                        break;

		case 3:
                        System.out.println("Wednsday");
                        break;

		case 4:
                        System.out.println("Thursday");
                        break;

		case 5:
                        System.out.println("Friday");
                        break;

		case 6:
                        System.out.println("Saturday");
                        break;
		default:
                        System.out.println("Default");
                        break;



	}

  }
 }
}

 BIN +1.17 KB FahrenheittoCelsius.class 
Binary file not shown.
 16  FahrenheittoCelsius.java 
@@ -0,0 +1,16 @@
import java.util.*;
public class FahrenheittoCelsius
{
	public static void main(String arg[])
	{
	    double a;
             	    Scanner sc=new Scanner(System.in);
	    System.out.println("Enter  Fahrenheit temperature");
                   a=sc.nextDouble();
	    System.out.println("Celsius temperature is = "+celsius(a));
	}
	static double celsius(double f)
	{
	return  (f-32)*5/9;
	}
}
 BIN +1 KB Fibonacci.class 
Binary file not shown.
 17  Fibonacci.java 
@@ -0,0 +1,17 @@
public class Fibonacci
{
public static void main(String args[])
{
 int n1=0,n2=1,n3,i,count=10;
 System.out.print(n1+" "+n2);

 for(i=2;i<count;++i)
 {
  n3=n1+n2;
  System.out.print(" "+n3);
  n1=n2;
  n2=n3;
 }

}
}
 BIN +1.23 KB Perfect.class 
Binary file not shown.
 27  Perfect.java 
@@ -0,0 +1,27 @@
import java.util.Scanner;
public class Perfect
{
public static void main(String args[])
{
int n, sum=0;
Scanner sc=new Scanner(System.in);
System.out.print("Enter the number: ");
n=sc.nextInt();
int i=1;

while(i <= n/2)
{
if(n % i == 0)
{
sum = sum + i;
}
i++;
} 
if(sum==n)
{
System.out.println(n+" is a perfect number.");
} 
else
System.out.println(n+" is not a perfect number.");
}
}
 BIN +499 Bytes Prime.class 
Binary file not shown.
 15  Prime.java 
@@ -0,0 +1,15 @@
public class Prime
{
	public static void main(String[] args)
	{
		int i=3;
		if(i%2==0)
		{
			System.out.println("Prime number");
		}
		else
		{
			System.out.println("Not a primenumber");
		}
	}
}
 BIN +1.1 KB PrimeNumber.class 
Binary file not shown.
 27  PrimeNumber.java 
@@ -0,0 +1,27 @@
public class PrimeNumber
{
 public static void main(String args[]){
  int i,m=0,flag=0;
  int n=4;
  m=n/2;
  if(n==0||n==1){
   System.out.println(n+" is not prime number");
  }
  else
  {
   for(i=2;i<=m;i++)
   {
    if(n%i==0)
    {
     System.out.println(n+" is not prime number");
     flag=1;
     break;
    }
   }
   if(flag==0)
   {
	System.out.println(n+" is prime number");
   }
  }
}
}
 BIN +946 Bytes ReverseNo.class 
Binary file not shown.
 16  ReverseNo.java 
@@ -0,0 +1,16 @@
public class ReverseNo
{
	public static void main(String[] args)
	{
		int n=1234;
		int rev=0;
		while(n!=0)
		{
		int rem=n%10;
		rev=rev*10+rem;
                n=n/10;

		System.out.println("reverse number is:" +rev);
		}
	}
}
 BIN +1.56 KB StopWatch.class 
Binary file not shown.
 45  Stopwatch.java 
@@ -0,0 +1,45 @@
import java.util.Scanner;
public class StopWatch
{
	public long startTimer=0;
        public long stopTimer=0;
        public long elapsed;

	//to start timer
	public void start()
	{
		startTimer=System.currentTimeMillis();
		System.out.println("Start Time is: "+startTimer);
	}

	// to stop timer
	public void stop()
	{
		stopTimer=System.currentTimeMillis();
		System.out.println("Stop Time is: "+stopTimer);
	}

	public long getElapsedTime()
	{
		elapsed=stopTimer-startTimer;
		return elapsed;
	}

	public static void main(String[] args) 
	{
		StopWatch sw=new StopWatch();
		System.out.println("Press '1' to Start Time: ");
		sw.start();

		System.out.println();
		System.out.println("Press '2' to Stop Time: ");

		sw.stop();

		long l=sw.getElapsedTime();
		System.out.println();
		System.out.println("Total Time Elapsed(in millisec) is:"+l);
		System.out.println();
		System.out.println("Converting millisec to seconds: "+(l/1000)+" sec");
	}
}
 BIN +1.52 KB VendingMachine.class 
Binary file not shown.
 52  VendingMachine.java 
@@ -0,0 +1,52 @@
import java.util.*;

public class VendingMachine
{
	// Static Variables i for indexing the array and total for calculating the total Notes
  	static int i=0;
  	static int total=0;

  	//Initialization of New Array
  	static int[] notes = { 1000,500,100,50,10,5,2,1};
  	static int money;

  	// Function for Calculating the notes
  	public static  int calculate(int money,int[]notes )
  	{
  		//calling calculate Function
 	int rem;
		if(money==0)
		{
			return -1 ;
		}
		else
		{
			if(money>=notes[i])
			{
				// logic for Calculating The notes
				int calNotes =money/notes[i];
				rem = money%notes[i];
				money =rem;
				total += calNotes;
				System.out.println(notes[i]+   " Notes ---> " +calNotes );
			}
			return calculate(money, notes);
		}
	}//end of method

  	// Starting Main Function
	public static void main(String[] args)
	{
        Scanner u1=new Scanner(System.in);

		//ask the user enter the money
		System.out.print("Enter the Amount:");
		int money=u1.nextInt();

		// Creating The Object of Vending MAchine class
		VendingMachine.calculate(money,notes);
		System.out.println("Total Number of Notes are :"+total);
	}
}

