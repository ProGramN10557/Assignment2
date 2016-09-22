class Person {
	int age;
	boolean gender;// false --> male, true --> female

	Person(int age, boolean gender) {
		this.age = age;
		this.gender = gender;
	}
}

public class Assignment2 {
	// Assignment
	/**
	 * Write a Computer program to find the type of a person and print the type.
	 * Infant : If the age is less than 1 year Toddler : If the age is less than
	 * 3 and greater than 1 Pre Schooler : If the age is less than 5 and greater
	 * than 3 KG Girl : If the age is greater than 5 and less than 6 and the
	 * gender is female KG Boy : If the age is greater than 5 and less than 6
	 * and the gender is male
	 */
	public void personType(Person person) {
    		if (person.age < 1) 
    		System.out.println("Infant");
    		if (person.age > 1&& person.age < 3  )
    		System.out.println("Toddler");
    		if (person.age > 3 && person.age < 5   )
    		System.out.println("Pre Schooler");
    		if (  person.age > 5&& person.age < 6 &&  person.gender == true)
    		System.out.println("KG Girl");
    		if (person.age > 5&& person.age < 6   &&  person.gender == false)
    		System.out.println("KG Boy");
    }
    

	/**
	 * Given an integer N as input, check the following: If N is odd, print
	 * "Weird". If N is even and, in between the range of 2 and 5(inclusive),
	 * print "Not Weird". If N is even and, in between the range of 6 and
	 * 20(inclusive), print "Weird". If N is even and N>20, print "Not Weird".
	 */
	public void weirdNumber(int n) {
    		if (n%2 != 0) 
		System.out.println("Weird");
		if (n >= 2 && n <= 5 && n%2 == 0  )
		System.out.println("Not Weird");
		if (n >= 6 && n <= 20 && n%2 == 0   )
		System.out.println("Weird");
		if (n > 20 && n%2 == 0 )
		System.out.println("Not Weird");
	}

	/**
	 * Write a method to determine whether a number is prime
	 */
	public void isPrime(int n) {
                boolean Prime = true;
    		if (n < 2) {
    		System.out.println("The Number entered is NOT a Prime Number");
    		}
    		else if(n == 2) {
    		System.out.println("The number entered is a Prime Number");
    		}
    		else{
		b=n/2
    		for(int i = 2; i <= b; i++){  	
    			if(n%i == 0) {
    			Prime = false;
    			break;
    			}
    		}
    		if(Prime == true){
	    	System.out.println("The number entered is a Prime Number ");
    		}
    		else{
    		System.out.println("The Number entered is NOT a Prime Number ");
    		}
  	    }
	}
	

	/**
	 * Find N fibonacci numbers Fibonacci Number: f(N) = f(N-1)+f(N-2).
	 * Typically, f(0)=f(1)=1.
	 */
	public int[] fibonacciNumber(int n) {
		int[] FibNum = new int[n+2];
		if (n < 0) {
			System.out.println("please ensure that number you have entered is positive number");
		}
		if (n == 0) {
			FibNum[0] = 1;
		}
		if (n == 1) {
			FibNum[0] = 1;
			FibNum[1] = 1;
		}
		FibNum[0] = 1;
		FibNum[1] = 1;
		for(int i = 2; i < n;i++) {
			FibNum[i] = FibNum[i-1] +FibNum[i-2];
		}
		
		return FibNum;
	}

	/**
	 * Write a function that takes a string as input and returns the string
	 * reversed. Given s = "hello", return "olleh".
	 */
	public String reverseString(String s) {
		char[] in = s.toCharArray();
		int begin=0
		int end=in.length-1
		char temp
		while (end>begin){
		temp=in[begin];
		in[begin]=in[end];
		in[end]=temp;
		end--;
		begin++;
		}
		Return new string(in);
	}
		
	/**
	 * Given an array of nums, write a function to find the largest two integer.
	 */
	public int[] findTheLargestTwo(int[] nums) {
 	
	Int[] result = new int[2];
	Int LargeOne = 0;
	Int LargeTwo = 0;
	
	For (int i=0; i<nums.length;i++) {
	
	If(nums[i] > LargeOne){
	LargeTwo=LargeOne
	LargeOne=nums[i]
	}
	}
	Result[0] = LargeOne;
	Result[1]=LargeTwo;
	Return result;}

	/**
	 * Given an array nums, write a function to move all 0's to the end of it
	 * while maintaining the relative order of the non-zero elements. For
	 * example, given nums = [0, 1, 0, 3, 12], after calling your function, nums
	 * should be [1, 3, 12, 0, 0].
	 */
	public void moveZeroes(int[] nums) {
            int count = 0;
	    int i = 0;
	    for(int j = 0; j < nums.length;j++){
	        if(nums[j]==0){
	        	count++;
	        }
	        else{
	            nums[i]=nums[j];
	            i++;
	        }
	    }
	    
	    for(int n = i; n < nums.length; n++){
	        nums[n] = 0;
	    }
	    return;
	}

	// Bonus
	/**
	 * Given a non-negative integer n, repeatedly add all its digits until the
	 * result has only one digit. For example: Given n = 38, the process is
	 * like: 3 + 8 = 11, 1 + 1 = 2. Since 2 has only one digit, return it.
	 */
	public int addDigits(int n) {
		   int sum = 0;
    while (n > 9 ) {
                 sum=0;
        while (n > 0) {
            int remainder;
            remainder = n % 10;
            sum = sum + remainder;
            n = n / 10;
        }
        n = sum;
    }

    Return n;
}

	/**
	 * Write a program to check whether a given number is an ugly number. Ugly
	 * numbers are positive numbers whose prime factors only include 2, 3, 5.
	 * For example, 6, 8 are ugly, while 14 is not ugly since it includes
	 * another prime factor 7. Note that 1 is typically treated as an ugly
	 * number.
	 */
	public boolean isUgly(int n) {
		
    		if (n == 1) {return true;}
if (n <= 0) {return false;}
    		if (n % 2 == 0) {
        		return isUgly(n/2);	
    		}
    		if (n % 3 == 0) {
        		return isUgly(n/3);
    		}
    		if (n % 5 == 0) {
        		return isUgly(n/5);
    		}
    			return false;   
		}

