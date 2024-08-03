[[Javascript]] | [[Conceptos de programación]]

#### Bucle For
```javascript
for (let i = 0; i < 10; i++) {
	console.log(i);
}
```
#### Bucle While 
```javascript
let i = 0;
while (i < 10) {
	console.log(i);
	i++;
}
```
#### Bucle Do-While
```javascript
let j = 0;
do {
	console.log(j);
	j++;
} while(j < 10);
```
#### Bucle For ... of
```javascript
let arr = [1,2,3];
for (let value of arr) {
	console.log(value);
}
```
#### Bucle For ... in (for Objects)
```javascript
let obj = { a: 1, b: 2, c: 3};
for (let key in obj) {
	console.log(key, obj[key]);
}
```