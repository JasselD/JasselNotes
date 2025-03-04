- <mark style="background: #ABF7F7A6;">A thread of execution in a program</mark> (kind of like a virtual CPU)
- JVM(Java Virtual Machine) allows an application to have <mark style="background: #ABF7F7A6;">multiple threads running simultaneously</mark>
- Each thread has a priority and threads with higher priority are executed in preference compared to threads with lower priority 
	- <mark style="background: #ABF7F7A6;">Higher the number of priority the thread is, the higher the priority it gets (The scale is 1-10, 10 being the highest priority)</mark>
- JVM will continue to execute threads until either of these happen
	- Exit method of class Runtime has been called
	-  All user threads have died
- There are two types of thread
	- <mark style="background: #ABF7F7A6;">Daemon thread</mark>
	    - <mark style="background: #ABF7F7A6;">A low priority thread</mark> that run in the background to perform tasks such as garbage collection
	- <mark style="background: #ABF7F7A6;">User thread</mark>
		- JVM terminates itself when all user threads <mark style="background: #ABF7F7A6;">finish their execution</mark>

**Methods
- Set name 
	- Thread.currentThread().setName("name");
- Set priority
	-  Thread.currentThread().setPriority();
- Get name
	-  Thread.currentThread().getName();
- Get priority
	-  Thread.currentThread().getPriority();
- Sleep 
	- Thread.sleep(milliseconds);
- To check what kind of thread
	- thread.isDaemon(); 
- To set to Daemon thread
	- thread.setDaemon(true);

**Creating and starting a thread
```Java
public class main {
	public static void main(String[] args) {
		MyThread thread2 = new MyThread(); // Creating a new thread

		thread2.start(); // Starting the thread

		System.out.println(thread2.isAlive()); // Checking if the thread is running
	}
}
```

```Java
public class MyThread extends Thread {
	@Override
	public static void run(){
		System.out.println("This thread is running");
	}
}
```


[[Multithreading]]