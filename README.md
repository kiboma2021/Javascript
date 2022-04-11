1. Write a JavaScript function to print the “Hello World” message

	function Greeting(){
		console.log("Hello World");
	}

2. Write a function that returns the square of a number

	function SquareNum(n){
		return n*n;
	}
	console.log(SquareNum(15));

3. Write a function to convert Celsius to Fahrenheit based on the formula (Celsius × 9/5) + 32 = Fahrenheit

	function CelFar(celcious){

		return ((celcious*9/5)+32);
	}
	console.log(CelFar(20));

4. Write a function to find the area of a given Rectangle given width and height

	function RectangleArea(w,h){
		//return (w*h);
		return `The area of the rectangle is ${w*h}`;
	}
	console.log(RectangleArea(10,5));

5. Write a function to find the area and perimeter of a Circle

	function Circle(r){
		return `The are of the circle is ${22/7*r*r} and perimeter ${22/7*2*r}`;
	}
	console.log(Circle(13));

	NB: Math.PI is equivalent to 22/7


6. Write a function to reverse a number

	function reverseNum(num){
		let originalNum=num;
		let reversedNum=0;
		while (num>0){
			reversedNum=reversedNum*10;
			remainder=num%10;
			reversedNum=reversedNum+remainder;
			num=Math.floor(num/10);
		}
		return `The reversed number for ${originalNum} is ${reversedNum}`;
	}
	console.log(reverseNum(4567843));


7. Count number of Vowels in String

	function countvowels(str)
	{

	  str=str.toLowerCase();
	  count=0;
	  for(let i=0;i<str.length;i++)
	  {
	    if(str[i]=='a'||str[i]=='e'||str[i]=='i'||str[i]=='o'||str[i]=='u')
	    count++;
	  }
	  return `The number of vowels in the string is: ${count}`
	}
	console.log(countvowels("Ben Wa Kiboma WA Omayio"))

8. Flatten array of arrays using JavaScript reduce


	function flattenArr(Arr){
		return Arr.reduce((result,array)=>result.concat(array));
	}
	console.log(flattenArr([[12,123,234,24],[23,34,11,22],[34,34,11,22],[11,33,55,66]]));


9. Write a function to check if an input string is a palindrome

	function checkPalindrome(str)
	{
	  str=str.toLowerCase();
	  for(let i=0;i<str.length;i++)
	  {
	    if(str[i]!=str[str.length-i-1])
	    {
	      return `The string ${str} is not palindrome`;
	    }

	  }
	  return `The string ${str} is a palindrome`;
	}

	console.log(checkPalindrome("maDam"));
	console.log(checkPalindrome("seito"));
	console.log(checkPalindrome("323"));

10. Write a function to calculate simple interest based on the principle amount

	function simpleinterest(principal,rate,time){
		return `Simple interest is: ${principal*rate*time}`;
	}
	console.log(simpleinterest(12000,0.34,12));

11. Write a function to calculate compound interest based on the principle amount

	function compoundinterest(principal,rate,time){
		let ci=principal*Math.pow((1+rate),(time));
		return `Compound interest is: ${ci}`;
	}
	console.log(compoundinterest(12000,0.12,10));

12. Write a function to generate a random number(return a generated random integer number between the provided start and end range).

	function GenerateRandom(start,end){
		let randomnum=Math.floor(Math.random()*end)+start;
		return `Random num between ${start} and ${end} is ${randomnum}`;
	}
	console.log(GenerateRandom(2,14));

13. Write a function to find Factorial of a number


	function getFactorial(num){
		if(num==1){
			return 1;
		}
		if(num==0 || num<0){
			return 0;
		}
		return num*getFactorial(num-1);
	}

	console.log(getFactorial(13));


14. Write a function to add unlimited numbers (the sum of all the number passed as arguments of the function)

	function AddUnlimitedNums(...args){
		return args.reduce((total,nums)=>total+nums);
	}
	console.log(AddUnlimitedNums(12,12,24,10));


15. Write a function to combine unlimited arrays

	function combineUnlimitedArrays(...args){
		return args.reduce((total,arrs)=>total.concat(arrs));
	}
	console.log(combineUnlimitedArrays([12,11,43],[12,55,67],[45,87,89]));


16. Write a function to find the count of a letter in a string

	function letterCount(str,c){
		str=str.toLowerCase();
		let count=0;
		for(let i=0;i<str.length;i++){
			if(str.charAt(i)==c){
				count++;
			}
		}
		return count;
	}
	
	console.log(letterCount('Hey Ben, Welcome to Javascript Exercises','e'));


17. Write a function to check if a number is Prime( return Boolean value based on whether the number is Prime or not )


	function checkPrime(num,div=2){
		if(num<=2){
			return (num==2)? true:false;
		}
		if(div*div>num){
			return true;
		}
		if(num%div==0){
			return false;
		}
		
		return (checkPrime(num,div+1));
	}

	console.log(checkPrime(31));
	console.log(checkPrime(33));
	console.log(checkPrime(11));
	console.log(checkPrime(6));

18. Reverse the provided string.
You may need to turn the string into an array before you can reverse it.
Your result must be a string.

	function reverseString(str){
		let reversedstr="";
		for(let i=str.length-1;i>=0;i--){
			reversedstr+=str[i];
		}
		return reversedstr;
	}
	console.log(reverseString("Hello Ben"));
	console.log(reverseString("Trial"));


19. Truncate a string (first argument) if it is longer than the given maximum string length (second argument). 
Return the truncated string with a ... ending.

	function truncateString(str,len){
		if(str.length<=len){
			return str;
		}
		return (str.slice(0,len)+"...");
	}
	
	console.log(truncateString("Ben Kiboma Omayio",10));


20. Return the lowest index at which a value (second argument) should be inserted into an array (first argument) once it has been sorted. 
The returned value should be a number.For example, getIndexToIns([1,2,3,4], 1.5) should return 1 because it is greater than 1 (index 0), 
but less than 2 (index 1). Likewise, getIndexToIns([20,3,5], 19) should return 2 because once the array has been sorted it will look like
[3,5,20] and 19 is less than 20 (index 2) and greater than 5 (index 1).


	function getIndextoInsert(arr,num){
		arr.sort((a,b)=>a-b);
		for(let i=0;i<arr.length;i++){
			if(arr[i]>=num){
				return i;
			}
		}
		return arr.length;
	}
	console.log(getIndextoInsert([12,11,23,45],13));

21. Write a function that splits an array (first argument) into groups the length of size (second argument) and returns them as a 
two-dimensional array.

	function splitArray(arr,size){
		if(arr.length<=size){
			return [arr];
		}
		return [arr.slice(0,size)].concat(splitArray(arr.slice(size),size));
	} 
	console.log(splitArray([12,3,12,12,45,66,477,88,12,11,24],3));


22. We'll pass you an array of two numbers. Return the sum of those two numbers plus the sum of all the numbers between them. 
The lowest number will not always come first. For example, sumAll([4,1]) should return 10 because sum of all the numbers 
between 1 and 4 (both inclusive) is 10.


	function SumArray(arr){
		let max=Math.max(arr[0],arr[1]);
		let min=Math.min(arr[0],arr[1]);
		let sumall=0;
		
		for(let i=min;i<=max;i++){
			sumall+=i;
		}
		return sumall;
	}
	console.log(SumArray([12,15]));


23. Print the first 10 Fibonacci numbers without recursion

	let f0=0;
	console.log(f0);
	let f1=1;
	console.log(f1);

	for(let i=2;i<=10;i++)
	{
	  fi=f0+f1;
	  console.log(fi);

	  f0=f1;
	  f1=fi;
	}




