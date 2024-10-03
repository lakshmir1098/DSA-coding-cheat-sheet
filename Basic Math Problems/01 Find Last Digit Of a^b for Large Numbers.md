## Question
You are given two integer numbers, the base a and the index b. You have to find the last digit of ab.Your task is to complete the function getLastDigit() which takes two strings a,b as parameters and returns an integer denoting the last digit of ab.

## Examples:

1. Input: a = "3", b = "10"
Output: 9
Explanation: 310 = 59049. Last digit is 9.
2. Input: a = "6", b = "2"
Output: 6
Explanation: 62 = 36. Last digit is 6.

## Solution Explanation
The problem with exponent should be handeld with `BigInteger` class.
1. Here using `BigInteger` class we find the power of a and b by  

## Solution
```java
 static int getLastDigit(String a, String b) {
        // code here
       BigInteger ab = new BigInteger(a);
       BigInteger bb =  new BigInteger(b);
       BigInteger modulus = BigInteger.TEN;
       
       BigInteger  result = ab.modPow(bb, modulus);
       
       return result.intValue();
       
       
       //simpler way to do this is
        return new BigInteger(a).modPow(new BigInteger(b), BigInteger.TEN).intValue();
    }
```