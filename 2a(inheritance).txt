
class A
{
	int i,j;
	void showij()
	{
		System.out.println("i="+i+" \nj="+j);
	}
}

class B extends A{
	int k;
	void showk()
	{
		System.out.println("k value is: "+k);
	}
	void show()
	{
		System.out.println(i+" "+j+" "+k);
		System.out.println(i+j+k);
	}
}
public class lab2 {
	public static void main(String args[])
	{
		A obj1 = new A();
		B obj2 = new B();
		obj1.i = 10;
		obj1.j = 20;
		System.out.println("content of class A : ");
		obj1.showij();
		obj2.i = 5;
		obj2.j = 3;
		obj2.k = 6;
		System.out.println("content of class B : ");
		obj2.showk();
		obj2.show();
	}
}
