# Given-an-integer-N-the-task-is-to-print-the-F-N-th-term-in-Java

Print F(N)th term in Java
Here, in this page we will discuss the program to print the F(N)th term in java.  A function f is defined as follows F(N)= (1) +(2*3) + (4*5*6) … N. We are given with an integer N and we need to print the F(N)th term.

Example :

Input : 4
Output : 5167
Explanation : 1 + (2*3) + (4*5*6) + (7*8*9*10) = 5167.
Print F(N)th term in Java
We can solve this using two methods that is listed below 

Using Recursion 
Using loop 
Method 1 (Using Recursion) :
Create a recursive function say term(int calculated, int current, int N)
Declare a variable cur to hold the product of the terms and initialize it with 1.
Base condition will be if(current == N+1) then, return 0. Here, current denotes the current term of the series.
Now, run a loop to calculate the product of terms till current.
Set i= calculate. Termination condition of the loop will be i>= calculated + current.
Inside loop set cur *= i
After execution of loop return cur + term(i, current+1, N)
Print F(N)th term in java
Java code
Run
class Main
{
  public static void main (String args[])
  {
    int n = 3;
    System.out.println (term (1, 1, n));
  }
// Recursive function 
  static int term (int calculated, int current, int N)
  {
    int i, cur = 1;
    // Base Condition
    if (current == N + 1)
      return 0;
    // product of terms till current
    for (i = calculated; i < calculated + current; i++)
      cur *= i;
    return cur + term (i, current + 1, N);
  }
}
Output :

127
Related Pages
Program to Find LCM

Program to find GCD

Program for octal to decimal conversion

Program for hexadecimal to decimal conversion

Program for decimal to binary conversion

Method 2 (Using Loop) :
Create a function say term(int calculated, int current, int N) to calculate the required N-th term.
Declare a variable result = 0.
Run a while loop till current != N+1.
Inside while loop declare a variable cur to hold the product of the terms and initialize it with 1.
Now, run a loop to calculate the product of terms till current.
Set i= calculate. Termination condition of the loop will be i>= calculated + current.
Inside for loop set cur *= i.
After execution of for loop set calculated = i, result += curr and increment current value by 1.
After the execution of while loop return result.
Note:
The tie complexity of this code is O(n) and the space complexity is O(1)
Java Code
Run
class Main
{
  public static void main (String args[])
  {
    int n = 3;
      System.out.println (term (1, 1, n));
  }
//Function to calculate N-th term
  static int term (int calculated, int current, int N)
  {
    int i, result = 0;
    while (current != N + 1)
      {
    int cur = 1;
    // product of terms till current
    for (i = calculated; i < calculated + current; i++)
      cur *= i;
    calculated = i;
    result += cur;
    current++;
      }
    return result;
  }
}
Output
127
