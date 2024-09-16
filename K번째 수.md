# 나의 풀이
* 배열을 자를 때, `Arrays.ofCopyRange(array, from, to)` 메서드를 사용한다.
```java
import java.util.*;
class Solution {
    public int[] solution(int[] array, int[][] commands) {
        int[] answer = new int[commands.length];
        
        for(int i = 0; i < answer.length; i++){
            int[] command = commands[i];
            int from = command[0] - 1;
            int to = command[1];
            int k = command[2]-1;
            
            int[] subArray = Arrays.copyOfRange(array, from, to);
            Arrays.sort(subArray);
            answer[i]  = subArray[k];
        }
        return answer;
    }
}
```