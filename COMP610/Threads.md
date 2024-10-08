- ==A thread of execution in a program== (kind of like a virtual CPU)
- JVM(Java Virtual Machine) allows an application to have multiple threads running simultaneously 
- Each thread has a priority and threads with higher priority are executed in preference compared to threads with lower priority 
	- Higher the number of priority the thread is, the higher the priority it gets (The scale is 1-10, 10 being the highest priority)
- JVM will continue to execute threads until either of these happen
	- Exit method of class Runtime has been called
	-  All user threads have died
- There are two types of thread
	- Daemon thread
	    - A thread that run in the background to perform tasks such as garbage collection
	- User thread

**Methods
- Set name 
	  - Thread.currentThread().setName("name");
- Set priority
	  - Thread.currentThread().setPriority();
- Get name
	  - Thread.currentThread().getName();
- Get priority
	  - Thread.currentThread().getPriority();
- Sleep 
	  - Thread.sleep(milliseconds);

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


