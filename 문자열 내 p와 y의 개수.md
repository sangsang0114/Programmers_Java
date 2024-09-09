# 나의 풀이
* 문자열 내에서 직접 개수를 구한다.
```java
class Solution {
    boolean solution(String s) {
        int pCount = 0;
        int yCount = 0;
        
        for(char c: s.toCharArray()){
            if(c == 'p' || c == 'P') ++pCount;
            else if(c == 'y' || c == 'Y') ++yCount;
        }

        return pCount == yCount;
    }
}
```

# 다른 사람의 좋은 풀이
* 모든 문자들을 대문자로 바꾼다.
* 모든 문자를 `s.chars()`를 이용해 유니코드값을 바꾼다음, 'P'만 남긴 개수와, 'Y'만 남긴 개수를 비교해서 true/false를 비교한다
```java
class Solution {
    boolean solution(String s) {
        s = s.toUpperCase();

        return s.chars().filter( e -> 'P'== e).count() == s.chars().filter( e -> 'Y'== e).count();
    }
}
```
