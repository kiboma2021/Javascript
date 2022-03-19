
1. Print the odd numbers less than 100

	for(let i=1;i<100;i+=2){
		console.log(i);
	}

2. A prime number is a whole number greater than 1 with exactly two divisors: 1 and itself. For example, 2 is a prime number 
because it is only divisible by 1 and 2. In contrast, 4 is not prime since it is divisible by 1, 2 and 4.
Rewrite sumPrimes so it returns the sum of all prime numbers that are less than or equal to num.


3. Javascript staircase

	function staircase(n) {
	    // Write your code here
	    for(let i=1;i<=n;i++)
	    {
	        // console.log("#")
	        console.log(" ".repeat(n-i) + "#".repeat(i));
	    }
	}
