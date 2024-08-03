[[Javascript]] | [[Conceptos de programación]]

#### Selección de elementos 
```javascript
let element = document.getElementById('id');
let elements = document.getElementByClassName('class');

let element = document.querySelector('selector');
let elements = document.querySelectorAll('selector');
```
#### Manipulación de elementos
```javascript
// Cambiar contenido
element.textContent = 'New Content';
element.innerHTML = '<p>New Content</p>';

// Cambio de estilo
element.style.color = 'red';

// Detector de eventos
element.addEventListener('click', function() {
	console.log('Element clicked!');
});
```