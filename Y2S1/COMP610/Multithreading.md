- Process of executing multiple threads simultaneously
- Helps maximise utilisation of CPU
- Threads are independent, they don't affect the execution of other threads
- An exception in one thread will not interrupt other threads, this is useful for serving multiple clients
- Two ways of creating multithreads
	- extends Thread (Can only be subclass of one class)
	- implements Runnable (can extend to any other class + can implement other things)

```Java
public class Multithreading {

	public static void main(String[] args) {
		Multithread2 Thing = new Multithread2();
		Multithread2 Thing2 = new Multithread2();

		Thing.start();
		Thing2.start();
	}
}

public class Multithread2 {
    @Override
    public void run() {
        for(int i = 1; i <= 10; i++) {
            System.out.println(i);
            try {
                Thread.sleep(1000);
            } catch (InterruptedException ex) {
	            Logger.getLogger(Multithread2.class.getName()).log(Level.SEVERE, null, ex);
            }
        }
    }
}
```
Use .start() if you want to use 2 concurrent thread at the same time

