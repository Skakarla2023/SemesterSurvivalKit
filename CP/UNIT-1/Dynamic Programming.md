# 🌟 Dynamic Programming (DP)

- Dynamic Programming is about breaking a big problem into smaller sub-problems, solving each once, and reusing their results instead of solving again.
- It avoids repeated work by storing solutions (in a table or array).

### When to Use:

- Problem has overlapping subproblems (you keep solving the same smaller problems again and again).

- Problem has optimal substructure (solution of bigger problem can be built from smaller ones).


```java
public class Fibonacci_DP {
    public static int fibonacci(int n) {
        int dp[] = new int[n+1];
        dp[0] = 0;
        dp[1] = 1;

        for (int i = 2; i <= n; i++) {
            dp[i] = dp[i-1] + dp[i-2]; // reuse previous results
        }
        return dp[n];
    }

    public static void main(String[] args) {
        int n = 10;
        System.out.println("Fibonacci of " + n + " = " + fibonacci(n));
    }
}
```

