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
