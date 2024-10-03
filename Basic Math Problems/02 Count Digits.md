## Question
Given a number n. Count the number of digits in n which evenly divide n. Return an integer, total number of digits of n which divides n evenly.

Note :- Evenly divides means whether n is divisible by a digit i.e. leaves a remainder 0 when divided.
 

## Examples:
1. Input: n = 12
Output: 2
Explanation: 1, 2 when both divide 12 leaves remainder 0.
2. Input: n = 2446
Output: 1
Explanation: Here among 2, 4, 6 only 2 divides 2446 evenly while 4 and 6 do not.
3. Input: n = 23
Output: 0
Explanation: 2 and 3, none of them divide 23 evenly.

## Solution Explanation
1. Find the way to conver int/number into int array
2. Iterating through each element in find if the number is dividible (%) with the elem

## Solution
```java
static int evenlyDivides(int N){
       
    int count = 0;
    int arr[] =  Arrays.stream(String.valueOf(N).split("")) 
                    .mapToInt(Integer::parseInt) 
                    .toArray();
                    
    for ( int i = 0 ; i < arr.length; i++){
        if(arr[i]!=0 && N % arr[i]==0){
            count ++;
        }
    }
    
    return count;
}
```