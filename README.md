# Easy-Pronunciation

# Problem
Words that contain many consecutive consonants, like "schtschurowskia", are generally considered somewhat hard to pronounce.

We say that a word is hard to pronounce if it contains 4 or more consonants in a row; otherwise it is easy to pronounce. For example, "apple" and "polish" are easy to pronounce, but "schtschurowskia" is hard to pronounce.

You are given a string S consisting of N lowercase Latin characters. Determine whether it is easy to pronounce or not based on the rule above — print YES if it is easy to pronounce and NO otherwise.

For the purposes of this problem, the vowels are the characters  {a,e,i,o,u} and the consonants are the other 21 characters.

# Input Format
The first line of input will contain a single integer T, denoting the number of test cases.
Each test case consists of two lines of input.

The first line of each test case contains a single integer N, the length of string S.

The second line of each test case contains the string S.

# Output Format

For each test case, output on a new line the answer — YES if S is easy to pronounce, and NO otherwise.

Each character of the output may be printed in either uppercase or lowercase. For example, the strings YES, yeS, yes, and YeS will all be treated as identical.

# CODE
    /* package codechef; // don't place package name! */
    
    import java.util.*;
    import java.lang.*;
    import java.io.*;
    
    /* Name of the class has to be "Main" only if the class is public. */
    class Codechef
    {
    	public static void main (String[] args) throws java.lang.Exception
    	{
    		// your code goes here
    		Scanner sc = new Scanner(System.in);
    		int t = sc.nextInt();
    		while(t-->0){
    		    int c = 0;
    		    int n = sc.nextInt();
    		    String s = sc.next();
    		    for(int i=0;i<n;i++){
    		        if(s.charAt(i)!='a' && s.charAt(i)!='e' && s.charAt(i)!='i' && s.charAt(i)!='o' && s.charAt(i)!='u'){
    		            c++;
    		        }
    		        else{
    		            c=0;
    		        }
    		        if(c>=4){
    		            System.out.println("NO");
    		            break;
    		        }
    		    }
    		    if(c!=4){
    		        System.out.println("YES");
    		    }
    		}
    	}
    }
