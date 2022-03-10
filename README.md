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














