# LEETCODE-Strings-3110
Certainly! Let's perform a dry run of the provided `scoreOfString` method from the `Solution` class with a sample input to understand how it works step-by-step. Here’s the method again for reference:

```java
class Solution {
    public int scoreOfString(String s) {
        int n = s.length();
        int j = 1;
        int sum = 0;
        for (int i = 0; i < n - 1; i++) {
            sum += Math.abs((s.charAt(i) - '0') - (s.charAt(j) - '0'));
            j++;
        }
        return sum;
    }
}
```

Let's perform a dry run using the example input string `s = "12345"`.

### Initial State:
- `s = "12345"`
- `n = s.length() = 5`
- `j = 1`
- `sum = 0`

### Iteration Details:

1. **First iteration (`i = 0`):**
   - `s.charAt(i) = '1'` and `s.charAt(j) = '2'`
   - Calculate `Math.abs(('1' - '0') - ('2' - '0')) = Math.abs(1 - 2) = 1`
   - Update `sum = 0 + 1 = 1`
   - Increment `j = 1 + 1 = 2`

2. **Second iteration (`i = 1`):**
   - `s.charAt(i) = '2'` and `s.charAt(j) = '3'`
   - Calculate `Math.abs(('2' - '0') - ('3' - '0')) = Math.abs(2 - 3) = 1`
   - Update `sum = 1 + 1 = 2`
   - Increment `j = 2 + 1 = 3`

3. **Third iteration (`i = 2`):**
   - `s.charAt(i) = '3'` and `s.charAt(j) = '4'`
   - Calculate `Math.abs(('3' - '0') - ('4' - '0')) = Math.abs(3 - 4) = 1`
   - Update `sum = 2 + 1 = 3`
   - Increment `j = 3 + 1 = 4`

4. **Fourth iteration (`i = 3`):**
   - `s.charAt(i) = '4'` and `s.charAt(j) = '5'`
   - Calculate `Math.abs(('4' - '0') - ('5' - '0')) = Math.abs(4 - 5) = 1`
   - Update `sum = 3 + 1 = 4`
   - Increment `j = 4 + 1 = 5`

### End State:
- The loop completes as `i` has reached `n - 1`.
- The final value of `sum` is `4`.

### Return:
- The method returns `4`.

Thus, for the input string `"12345"`, the `scoreOfString` method returns a score of `4`.

This method computes the sum of the absolute differences between each pair of consecutive digits in the string. The dry run confirms the correctness of the method for this particular input.
