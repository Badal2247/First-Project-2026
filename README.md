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
                                                    //Palindrome Method.
                                                    
public static boolean array(){
    System.out.println("Enter your size of array: ");
    int n=sc.nextInt();
    int[]arr=new int[n];
    for(int i=0;i<n;i++){
        System.out.println("Enter your element "+(i+1)+":");
        arr[i]=sc.nextInt();
    }
    int i=0,j=n-1;
    boolean pali=true;
    while(i<j){
        if(arr[i]!=arr[j]){
            pali = false;
            break;
            
        }
        i++;
        j--;
    }
    return pali;
    
 }
                                                    //Fibonacci Method.
                                                    

public static void fibo(){
    System.out.println("Enter your terms: ");
    int n=sc.nextInt();
    int a=0,b=1,c=0;
    System.out.print(a+" "+b+" ");
    for(int i=2;i<n;i++){
        c=a+b;
        a=b;
        b=c;
        System.out.print(c+" ");
    }

}



                                                    //Factorial Method.

public static long factorial(int n){
    long fact=1;
    if(n<0){
        throw new IllegalArgumentException("Factorial is not defined for negative numbers.");
    }
    else if(n>20){
        throw new ArithmeticException("Factorial too large for long");
    }
    
    for(int i=1;i<=n;i++){
        fact*=i;
    }
    return fact;
}
                                                    //Multiple Opeartion on array.
public static void numop(){
    
                                                    //TAKING ARRAY INPUT
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
    System.out.println("================ Data ===============");
    System.out.println();
    System.out.println();
    
                                                    //DATA IN ARRAY
    
    System.out.println("Your array: ");
    for(int x: arr){
        System.out.print(x+" ");
    }
    System.out.println();
    System.out.println();
    
                                                    //OP1- REVERSE ARRAY
    
    System.out.println("Reverse array: ");
    for(int i=n-1;i>=0;i--){
        System.out.print(arr[i]+" ");
    }
    
    
    System.out.println();
    System.out.println();
    
                                                    //OP2- SUM OF ELEMENT
    
    System.out.println("=======================================");
    System.out.print("Sum of element: "+sum);
    System.out.println();
    
    int even=0,odd=0;
    
                                                    //OP3- EVEN NUMBERS
    
    System.out.print("Even numbers: ");
    for(int i=0;i<n;i++){
        if(arr[i]%2==0){
            System.out.print(arr[i]+" ");
            even++;
        }
    }
    
                                                    //OP4- ODD NUMBERS
    
    System.out.println();
    System.out.print("Odd numbers: ");
    for(int i=0;i<n;i++){
        if(arr[i]%2!=0){
            System.out.print(arr[i]+" ");
            odd++;
        }
    }
    
                                                    //OP5- PRIME NUMBERS
    
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
    
                                                    //OP6- NEGATIVE NUMBERS
    int neg=0;
    System.out.print("Negative numbers: ");
    for(int i=0;i<n;i++){
        if(arr[i]<0){
            System.out.print(arr[i]+" ");
            neg++;
        }
    }
    System.out.println();
    System.out.println("=======================================");
    
    System.out.println();
    
                                                    //OP7- COUNTING ZEROS
    
    int zero=0;
    for(int i=0;i<n;i++){
        if(arr[i]==0){
            zero++;
        }
    }
    
                                                    //OP8- MAX ELEMENT
    
    int max=arr[0];
    for(int i=1;i<n;i++){
        if(arr[i]>max){
            max=arr[i];
        }
    }
    
                                                    //OP9 - FACTORIAL OF EACH ELEMENT
    
    for(int i=0;i<n;i++){
        System.out.println("Factorial of "+arr[i]+":");
        try{
        System.out.println(factorial(arr[i]));
        } catch(Exception e){
            System.out.println(e.getMessage());
        }
    }
    
    System.out.println("=============== Details ===============");
    
    System.out.println();
    System.out.println("Total Even Numbers: "+even);
    System.out.println("Total Odd Numbers: "+odd);
    System.out.println("Total negative numbers: "+neg);
    System.out.println("Total prime numbers: "+prime);
    System.out.println("Total Zeros: "+zero);
    System.out.println("Your maximum element: "+max);
    
    
    
}
public static void palindrome(int n){
    int original=n;
    int rev=0;
    
    while(n!=0){
        int rem=n%10;
        rev=rev*10+rem;
        n=n/10;
    }
    if(original==rev){
        System.out.println("Palindrome");
    }else{
        System.out.println("Not Palindrome");
    }
}

public static void digitcount(int n){
    int count=0;
    while(n!=0){
        int rem = n%10;
        count++;
        n=n/10;
    }
    System.out.println("Your number contain "+count+" digit");
}  
    
public static void unitconversion(int n){
    int F=(int)(n+33.8);
    System.out.println("Temperature in faranhite: "+F);
}


public static void main(String[] args) {
    numop();
}

