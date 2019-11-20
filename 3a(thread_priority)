class ThreadClass implements Runnable
{
	long click=0;
	Thread t;
	private volatile boolean running =true;	
	public ThreadClass(int p)
	{	
		t=new Thread(this);	
		t.setPriority(p);	
	}
	public void run()
	{
		while(running)	
		{
			click++;
		}
	}
	public void stop()
	{
		running =false;
	}
	public void start()	
	{
		t.start();
	}
}

public class lab3a {
public static void main(String args[])
{
	Thread.currentThread().setPriority(Thread.MAX_PRIORITY);
	ThreadClass hi1=new ThreadClass(Thread.NORM_PRIORITY + 2);
	ThreadClass hi2=new ThreadClass(Thread.NORM_PRIORITY -2);
	ThreadClass hi3=new ThreadClass(Thread.NORM_PRIORITY + 3);
	ThreadClass hi4=new ThreadClass(Thread.NORM_PRIORITY - 3);
	ThreadClass hi5=new ThreadClass(Thread.NORM_PRIORITY +4);
	hi1.start();
	hi2.start();
	hi3.start();
	hi4.start();
	hi5.start();
	System.out.println("thread one is alive:" +hi1.t.isAlive());
	System.out.println("thread two is alive:" +hi2.t.isAlive());	
	System.out.println("thread three is alive:" +hi3.t.isAlive());
	System.out.println("thread four is alive:" +hi4.t.isAlive());
	System.out.println("thread four is alive:" +hi5.t.isAlive());
	try
	{ 
		hi5.t.sleep(1000);
		hi3.t.sleep(1000);
	}
	catch(InterruptedException e){
		System.out.println("main thread interrupted");
	}
	hi1.stop();
	hi2.stop();
	hi3.stop();
	hi4.stop();
	hi5.stop();
	try
	{
		System.out.println("waiting for threads to finish");
		hi1.t.join();
		hi2.t.join();
		hi3.t.join();
		hi4.t.join();
		hi5.t.join();
	}
	catch(InterruptedException e)
	{
		System.out.println("main thread interrupted");
	}
	System.out.println("priority of thread1:" +hi1.t.getPriority());	
	System.out.println("priority of thread2:" +hi2.t.getPriority());
	System.out.println("priority of thread3:" +hi3.t.getPriority());
	System.out.println("priority of thread4:" +hi4.t.getPriority());
	System.out.println("priority of thread5:" +hi5.t.getPriority());
	System.out.println("thread one is alive:" +hi1.t.isAlive());	
	System.out.println("thread two is alive:" +hi2.t.isAlive());
	System.out.println("thread three is alive:" +hi3.t.isAlive());	
	System.out.println("thread four is alive:" +hi4.t.isAlive());
	System.out.println("thread five is alive:" +hi5.t.isAlive());
	System.out.println("main thread exiting");
	}
}
