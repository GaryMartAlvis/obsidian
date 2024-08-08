[[Javascript]] | [[Conceptos de programación]]

#### Declaración de función 
```javascript
function greet(name) {
	return 'Hello, ${name}!';
}
```
#### Expresión de función
```javascript
const greet = function(name) {
	return 'Hello, ${name}!';
}
```
#### Función de flecha
```javascript
const greet = (name) => 'Hello, ${name}!';
```

```JavaScript
function saludar() {
	console.log('Hola mundo');
}

// Llamar a la función
saludar();

function suma(num1, num2) {  // (num1, num2) son llamados PARÁMETROS
	return num1 + num2;
}

console.log(suma(2, 5));     // (2, 5) son llamados ARGUMENTOS 
```
