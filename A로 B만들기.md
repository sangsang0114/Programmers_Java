# 나의 풀이
```java
import java.util.*;
class Solution {
    private static Map<Character, Integer> toMap(String word){
        Map<Character, Integer> map = new HashMap<>();
        for(char c: word.toCharArray()){
            map.putIfAbsent(c, 0);
            map.put(c, map.get(c) + 1);
        }
        return map;
    }
    public int solution(String before, String after) {
        return toMap(before).equals(toMap(after)) ? 1 : 0;
    }
}
```
# 다른 사람의 좋은 풀이
```java
import java.util.Arrays;
class Solution {
    public int solution(String before, String after) {
        char[] a = before.toCharArray();
        char[] b = after.toCharArray();
        Arrays.sort(a);
        Arrays.sort(b);

        return new String(a).equals(new String(b)) ? 1 :0;
    }
}
```
