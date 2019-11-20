//method1

public class Outer {
	private int x = 10;
	protected int z = 30;
	class inner {
		private int x = 20;
		protected int z = 85;
	}
	public static void main(String args[])
	{
		Outer obj1 = new Outer();
		inner obj2 = new Outer().new inner();
		System.out.println(" through outer class, x = "+obj1.x);
		System.out.println(" through inner class, x = "+obj2.x);
	}
}

/* separate class */
class smtg()
{
	public static void main(String [] args)
	{
		Outer ob1 = new Outer();
		Outer.inner ob2 = new Outer().new inner();
		System.out.println("through diff class, z = "+ob1.z);
		System.out.println("through diff class, z = "+ob2.z);
	}
}



//method 2 

public class Outer {
	private int x = 10;
	protected int z = 30;
	class inner {
		private int x = 20;
		protected int z = 85;
	}
	public static void main(String args[])
	{
		Outer obj1 = new Outer();
		inner obj2 = new Outer().new inner();
		System.out.println(" through outer class, x = "+obj1.x);
		System.out.println(" through inner class, x = "+obj2.x);
    System.out.println(" through outer class, z = "+obj1.z);
		System.out.println(" through inner class, z = "+obj2.z);
	}
}
