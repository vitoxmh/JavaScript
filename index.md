## Tips Basicos de Javascript

###### Acceso directo al DOM
```javascript
document.querySelector('nombreClase');
document.querySelectorAll('nombreClase');
```

###### Remover clase a un elemento
```javascript
document.querySelector('nombreClase').classList.remove('className');
```

###### Agregar clase a un elemento
```javascript
document.querySelector('nombreClase').classList.add('className');
```

###### Agregar o Quitar clase segun estado de un elemento
```javascript
document.querySelector('nombreClase').classList.toggle('className');
```

###### Eventos

* click
* blur
* change


```javascript
document.querySelector('nombreClase').addEventlistener('evento', (e) => {

    // Codigo Aqui

});
```
###### Mas eventos revisar en Pagina [https://developer.mozilla.org/es/docs/Web/Events](https://developer.mozilla.org/es/docs/Web/Events)

### Recorrer Array y Objectos

###### Objectos con Map
```javascript
const frutas = [
    {id: 1, nombre: 'Manzana'},
    {id: 2, nombre: 'Pera'},
    {id: 3, nombre: 'Platano'},
    {id: 4, nombre: 'Limon'},
];
 
frutas.map(function(fruta) {
    console.log(fruta.nombre)
});
```

###### Array con forEach
```javascript
const frutas = ['Manzana', 'Pera', 'Platano', 'Limon', 'Piña'];
frutas.forEach(function(fruta, index) {
    console.log(`${index} : ${fruta}`);
});
```

### Atributos

###### Modificar Atributos
```javascript
document.querySelector('selector').setAttribute("nombreAtributo", "datoAtributo");
```

###### Obtener Atributos
```javascript
element.getAttribute(nombreAtributo);
```


###### Remover Atributos
```javascript
element.removeAttribute(nombreAtributo);
```

