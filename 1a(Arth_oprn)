
import java.util.Scanner;
public class Arithmetic {
	int a,b;
	Scanner S = new Scanner(System.in);
	Arithmetic()
	{
		System.out.println("Enter 2 integers\n");
		a = S.nextInt();
		b = S.nextInt();
	}
	void display()
	{
		System.out.println("add :: "+(a+b));
		System.out.println("sub :: "+(a-b));
		System.out.println("mul :: "+(a*b));
		System.out.println("div :: "+(a/b));
	}
	Arithmetic(float a1,float b1)
	{
		System.out.println("add :: "+(a1+b1));
		System.out.println("sub :: "+(a1-b1));
		System.out.println("mul :: "+(a1*b1));
		System.out.println("div :: "+(a1/b1));
	}
	void display(int x)
	{
		System.out.println("the square of "+x+" is "+(x*x));
	}
	public static void main(String args[])
	{
		Scanner S = new Scanner(System.in);
		Arithmetic a = new Arithmetic();
		System.out.println("integer operation :");
		a.display();
		System.out.println("floating operation :");
		float a1 = S.nextFloat();
		float a2 = S.nextFloat();
		Arithmetic arth = new Arithmetic(a1,a2);
		System.out.println("enter no to find square\n");
		int x = S.nextInt();
		a.display(x);
	}
}
