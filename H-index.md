# 나의 풀이
* h의 범위는 0부터 입력 받은 논문의 개수이며, 최댓값을 구해야 하므로 가장 큰 값부터 h의 조건을 만족하는지 검사해 나가며 가장 먼저 발견하는 값을 반환해야 한다.
```java
import java.util.*;
class Solution {
    private boolean isValid(int [] citations, int h){
        int idx = citations.length - h;
        return citations[idx] >= h;
    }
    
    public int solution(int[] citations) {
        Arrays.sort(citations);
        for(int h = citations.length; h >= 1; --h)
            if(isValid(citations,h))
                return h;
        return 0;
    }
}
```