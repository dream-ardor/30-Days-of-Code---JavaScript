Task: Given a number, n, determine and print whether it is prime or not prime.

Solution:
 ```javascript
 function processData(input) {
	let result = input.split("\n").slice(1).map(isPrime);

	function isPrime(input, i) {
		let messageArray = ["Not prime", "Prime"];
		if (input == 1) {
			return messageArray[0];
		}
		if (input == 2) {
			return messageArray[1];
		}
		if (input % 2 == 0) {
			return messageArray[0];
		}
		for (i = 3; i <= Math.sqrt(input); i += 2) {
			if (input % i == 0) {
				return messageArray[0];
			}
		}
		return messageArray[1];
	}
	console.log(result.join("\n"));
}
```
