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

	function countVowels(str){
		str=str.toLowerCase();
		let count=0;

		for (let i=0;i<str.length;i++){
			if(str.charAt(i)=='a' || str.charAt(i)=='e' || str.charAt(i)=='i'
			||str.charAt(i)=='o' || str.charAt(i)=='u'){
				count++;
			}
		}
		return 'The entered str has ${count} vowels`;
	}
	console.log(countVowels(BenKIBomaOmayio));

8. Flatten array of arrays using JavaScript reduce


	function flattenArr(Arr){
		return Arr.reduce((result,array)=>result.concat(array));
	}
	console.log(flattenArr([[12,123,234,24],[23,34,11,22],[34,34,11,22],[11,33,55,66]]));


9. Write a function to check if an input string is a palindrome

	function checkpalindrome(str){
		for (let i=0;i<str.length;i++){
			if(str.charAt(i)!=str.charAt(str.length-i-1)){
				return `The string ${str} is not a palindrome`;
			}
		}
		return `The string ${str} is a palindrome`;
	}

	console.log(checkpalindrome('anana'));
	console.log(checkpalindrome('awanana'));
	console.log(checkpalindrome('madam'));

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




















