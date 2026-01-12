import  java.util.*;
public class Main{
    
    static Scanner sc=new Scanner(System.in);
                                                        //Printing Hello World.
    public static void hello(){
        System.out.println("Hello World");
    }
    
                                                        //Check Prime Method.
    public static boolean isprime(int n){
        
        if(n<2){
            return false;
        }
        int limit=(int)Math.sqrt(n);
        for(int i=2;i<=limit;i++){
            if(n%i==0){
                return false;
                
            }
        }
        return true;
    }
                                                        //Fibonacci Method.
                                                        
    public static int fibo(int n){
        if(n==0)return 0;
        if(n==1)return 1;
        int a=0,b=1;
        int c=0;
        for(int i=0;i<n-2;i++){
            c=a+b;
            a=b;
            b=c;
        }
        return c;
    }
    
                                                        //Factorial Method.
    
    public static long factorial(int n){
        long fact=1;
        if(n<0){
            throw new IllegalArgumentException("Factorial is not defined for negative numbers.");
        }
        
        for(int i=1;i<=n;i++){
            fact*=i;
        }
        return fact;
    }
                                                        //Multiple Opeartion on array.
    public static void numop(){
        System.out.print("Enter your size of array: ");
        int n=sc.nextInt();
        if(n<=0){
            System.out.println("Invalid size.");
            return;
        }
        int[] arr=new int[n];
        int sum=0;
        for(int i=0;i<n;i++){
            System.out.print("Enter your element "+(i+1)+":");
            arr[i]=sc.nextInt();
            sum+=arr[i];
        }
        System.out.println("================Data===============");
        System.out.println();
        System.out.println();
        System.out.println("Your array: ");
        for(int x: arr){
            System.out.print(x+" ");
        }
        System.out.println();
        System.out.println();
        System.out.println("Reverse array: ");
    
        for(int i=n-1;i>=0;i--){
            System.out.print(arr[i]+" ");
        }
        System.out.println();
        System.out.println();
        System.out.print("Sum of element: "+sum);
        System.out.println();
        
        int even=0,odd=0;
        
        System.out.print("Even numbers: ");
        for(int i=0;i<n;i++){
            if(arr[i]%2==0){
                System.out.print(arr[i]+" ");
                even++;
            }
        }
        System.out.println();
        System.out.print("Odd numbers: ");
        for(int i=0;i<n;i++){
            if(arr[i]%2!=0&&arr[i]!=0){
                System.out.print(arr[i]+" ");
                odd++;
            }
        }
        int prime=0;
        System.out.println();
        System.out.print("Your Prime Number: ");
        for(int i=0;i<n;i++){
            if(isprime(arr[i])==true){
                System.out.print(arr[i]+" ");
                prime++;
            }
        }
        System.out.println();
        int neg=0;
        System.out.print("Negative numbers: ");
        for(int i=0;i<n;i++){
            if(arr[i]<0){
                System.out.print(arr[i]+" ");
                neg++;
            }
        }
        System.out.println();
        int zero=0;
        for(int i=0;i<n;i++){
            if(arr[i]==0){
                zero++;
            }
        }
        int max=arr[0];
        for(int i=0;i<n;i++){
            if(arr[i]>max){
                max=arr[i];
            }
        }
        for(int i=0;i<n;i++){
            System.out.println("Factorial of "+arr[i]+":");
            try{
            System.out.println(factorial(arr[i]));
            } catch(Exception e){
                System.out.println(e.getMessage());
            }
        }
        System.out.println();
        System.out.println("Total Even Numbers: "+even);
        System.out.println("Total Odd Numbers: "+odd);
        System.out.println("Total negative numbers: "+neg);
        System.out.println("Total prime numbers: "+prime);
        System.out.println("Total Zeros: "+zero);
        System.out.println("Your maximum element: "+max);
    }
    
    
	public static void main(String[] args) {
	    
	}
}
