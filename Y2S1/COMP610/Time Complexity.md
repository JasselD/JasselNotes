- Amount of time for an algorithm to run
- Input processed by an algorithm determines the time complexity
```Java
public class TimeComplexityDemo {
	public static void main(String[] args) {
		double now = System.currentTimeMillis();
		TimeComplexityDemo demo = new TimeComplexityDemo();

		System.out.println("Time taken " + (Systen.currentTimeMillis() - now) + " millisecs");

		//this process takes less time
		public int findSum(int n) {
			return n * (n + 1) / 2;
		}

		//this process takes more time
		public int findSum(int n) {
			int sum = 0;
			for(int i = 0; i <= n; i++) {
				sum = sum + i;
			}
			return sum;
		}
	}
}
```

