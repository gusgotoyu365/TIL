
https://leetcode.com/problems/two-sum/

풀이
-------------
모든 배열을 돌면서 target과 같은 합이 있으면 그걸 답에 넣고 break하여 빠져나왔다.

Me (Poor English)
Explore every array and where is same value(nums sum of two index) as "target", if that appeared put that value in answer and escape with break.

GPT
Explore each element in the array, and if the sum of two indices matches the "target" value, add that value to "answer" and break out of the loop.

```java
class Solution {
    public int[] twoSum(int[] nums, int target) {
        int[] answer = {0, 0};
        for (int i=0; i<nums.length-1; i++) {
            for (int j=i+1; j<nums.length; j++) {
                if (nums[i]+nums[j] == target) {
                    answer[0] = i;
                    answer[1] = j;
                    break;
                }
            }
        }
        return answer;
    }
}
```

알고리즘 공부할 때 무슨 언어로 해야할지 못 고르겠어서 C#으로 일단 해보았다.<br>
제일 많이 쓰이는건 Java, Python, C++ 이라는데 선택이 어렵구나!<br>

I got deadrock when I have to choose programming language for Algorithm<br>
Most algorithm language seems Java, Python, C++ but I can't chooooooooooooooooooooooooooooooooooooooooose.

```Csharp
public class Solution {
    public int[] TwoSum(int[] nums, int target) {
        int[] answer = {0,0};
        for (int i=0; i<nums.Length-1; i++) {
            for (int j=1; j<nums.Length; j++) {
                if (nums[i] + nums[j] == target) {
                    answer[0] = i;
                    answer[1] = j;
                    break;
                }
            }
        }
        return answer;
    }
}
```

틀렸던거
-------------
아무생각 없이 i, j를 넣어주지 않고 nums[i], nums[j]를 넣어줘서 틀렸다.

Me
I thought useless way so I got wrong.

GPT
I approached it in an inefficient way, so I made a mistake.

```java
class Solution {
    public int[] twoSum(int[] nums, int target) {
        int[] answer = {0, 0};
        for (int i=0; i<nums.length-1; i++) {
            for (int j=i+1; j<nums.length; j++) {
                if (nums[i]+nums[j] == target) {
                    answer[0] = nums[i];
                    answer[1] = nums[j];
                }
            }
        }
        return answer;
    }
}
```