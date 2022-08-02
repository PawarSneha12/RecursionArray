# RecursionArray


First Question is Sum of digits in numbers
-----------
public class SumOFDigit {

    public static void main(String[] args){
        int ans= sumd(8452);
        System.out.println(ans);
        int ans1= productd(123);
        System.out.println(ans1);
    }
    
    static int sumd(int n){
        if(n==0){
            return 0 ;
        }
       return (n%10)+sumd(n/10);

    }
    static int productd(int n){
        if(n<=1){
            return 1 ;
        }
       return (n%10)*productd(n/10);

    }
    }
    ----------------------------------- 
    
    question 2.----
    // N to 1, 1 to n
    
    class NTO1{
    public static void main(String[] args){
       // FunN(6);
      // FunREV(5);

       FunBoth(5);
    }
    static void FunN(int n){
        if(n==0){
            return ;
        }
        System.out.println(n);
       FunN(n-1);
    }

    static void FunREV(int n){
        if(n==0){
            return ;
        }
       FunREV(n-1);
     
       System.out.println(" 1 to n number   "+n);
    }


    static void FunBoth(int n){
        if(n==0){
            return ;
        }
        System.out.println(n);
       FunREV(n-1);
     
      System.out.println(" 1 to n number   "+n);
    }}
    
    
    
    ----------------------------------
    
    question 3.
    //product of num
    
    public class Factorial {
    public static void main(String[] args){
      int ans= product(4);
       System.out.println(ans);
       int sum= SUMN(5);
       System.out.println(sum);
}
    static int product(int n){
        if(n<=1){
            return 1 ;
        }
       return n*product(n-1);
 }
    static int SUMN(int n){
        if(n==1){
            return 1 ;
        }
       return n+SUMN(n-1);
}}



----------------------------

question 4.
Reverse num and check polindrone or not

public class ReverseNum {
   
   //first way to reverse a number 
    static int sum=0;
    static void Rev(int n){
        if(n==0){
            return ; }
            int rem=n%10;
            sum=sum*10+rem;
            Rev(n/10);

           }  //second way by bit or helper function
    static int Rev1(int n){
          int digits=(int)(Math.log10(n)+1);
return helper(n, digits);
           } 
           static int helper(int n,int digit)
           {
            if(n%10==n){
                return n;
            }
            int rem=n%10;
            return rem*(int)(Math.pow(10,digit-1))+helper(n/10,digit-1);

           }
           //palindrone or not 
           static Boolean palindrone(int n){
            return (Rev1(n)==n);
           }

           public static void main(String[] args){
            //int ans=Rev1(12345);
            System.out.println(palindrone(123221));
          // System.out.println(ans);
    }}
    
    ---------------------------------------------------------------
    
    question 5.
    
    //Leetcode problem 1342
    //count the steps to reduce N to 0, when n is even devide by 2 otherwise substract by 1
    
    -->>
    public class Steps {
  
public static void main(String[] args){
            int ans=Steps1(41);
            System.out.println(ans);
        }
    
        static int Steps1(int n){
            return helper(n,0);
        }
    
    static int helper(int n,int step){
        if(n==0){
            return step;
        }
        if(n%2==0){
            return helper(n/2,step+1);
        }
        return helper(n-1,step+1);
    
    }
    }
    



Questions .5

//  Fibbo Series Using Recursion
class FibboSeries
{
    public static void main(String[]args){

        int ans=fibbo(4);
        System.out.println(ans);
    }
    
    static int fibbo(int n){

        if(n<2){
            return n;
        }
        return fibbo(n-1)+fibbo(n-2);
    }
}

------------------------------

questions 6.

//count zero in given numbers

-->
public class CountZeros {
    public static void main(String[] args){
        int ans =count(10090400);
        System.out.println(ans);
    }
    static int count(int n){
        return helper(n,0);
    }
    private static int helper(int n,int c){
        if(n==0){
            return c;
        }
       int rem=n%10;
       if(rem==0){
        return helper(n/10,c+1);
       }
       return helper(n/10,c);}}

-----------------------------





    
