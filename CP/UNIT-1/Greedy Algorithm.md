# 🌟 Greedy Algorithm

- A Greedy algorithm makes a series of choices, where at each step it picks the best option available at that moment (locally optimal), hoping this will lead to the global optimal solution.

### 👉 When to Use:

- Works when choosing the local best always leads to the global best.

- Faster and simpler than DP, but doesn’t always work.

### ✅ Example: Coin Change Problem

You want to make 27 using coins {25, 10, 5, 1}.

- Greedy approach:

Take biggest coin possible each time.

25 → 2 left → take 1 → total = 25 + 1 + 1 = 27.

```java
public class CoinChange_Greedy {
    public static void coinChange(int amount) {
        int coins[] = {25, 10, 5, 1};
        
        System.out.print("Coins used: ");
        for (int coin : coins) {
            while (amount >= coin) {
                amount -= coin;
                System.out.print(coin + " ");
            }
        }
    }

    public static void main(String[] args) {
        int amount = 27;
        coinChange(amount);
    }
}
```
