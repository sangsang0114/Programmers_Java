# 나의 풀이
* 2x1을 채우는 방법: 1
* 2x2를 채우는 방법: 블럭을 눕히기 + 블럭을 세우기 = 2
```java
import java.util.*;
class Solution {
    public int solution(int n) {
        final int MOD = 1_000_000_007;
        int[] dp = new int[n+1];
        dp[1] = 1;
        dp[2] = 2;
        for(int i = 3; i <=n; i++)
            dp[i] = (dp[i-1] % MOD + dp[i-2] % MOD ) % MOD;
        return dp[n];
    }
}
```