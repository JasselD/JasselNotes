- Make a program thread safe (counter race condition)
- Any synchorinzed block code needs a "monitor" object which is in charge of giving a thread the lock
- **Dont synchronize everything because it slows down the code

**Before synchronization (Rc)
```Java
class Counter {
    private int count = 0;

    public void increment() {
        count++;  // This is not thread-safe
    }

    public int getCount() {
        return count;
    }
}

public class RaceConditionExample {
    public static void main(String[] args) throws InterruptedException {
        Counter counter = new Counter();

        Thread t1 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) {
                counter.increment();
            }
        });

        Thread t2 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) {
                counter.increment();
            }
        });

        t1.start();
        t2.start();

        t1.join();  // Wait for thread t1 to finish
        t2.join();  // Wait for thread t2 to finish

        System.out.println("Final count: " + counter.getCount());
    }
}

```