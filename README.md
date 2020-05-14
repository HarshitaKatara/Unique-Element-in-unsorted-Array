# Unique-Element-in-unsorted-Array
//Given an array of integers. All numbers occur twice except one number which occurs once.//
//The best solution is to use XOR. XOR of all array elements gives us the number with single occurrence.//
//The idea is based on following two facts.
  a) XOR of a number with itself is 0.
  b) XOR of a number with 0 is number itself.//

//Let us consider the  example.//  
//Let ^ be xor operator as in C and C++.//

res = 7 ^ 3 ^ 5 ^ 4 ^ 5 ^ 3 ^ 4

//Since XOR is associative and commutative, above 
  expression can be written as:
  res = 7 ^ (3 ^ 3) ^ (4 ^ 4) ^ (5 ^ 5)  
    = 7 ^ 0 ^ 0 ^ 0
    = 7 ^ 0
    = 7 //

//Below are implementations of above algorithm.//

import java.io.*;
import java.util.*;

public class Solution {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int N = sc.nextInt();
        
        int a[] = new int[N];
        for(int i=0; i<N; i++){
            a[i] = sc.nextInt();
        }
        int res=a[0];
        for(int i=1; i<N; i++){
            res = res^a[i];
            
        }
        System.out.println(res);
        
    }
}
