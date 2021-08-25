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
* 
```javascript
document.querySelector('nombreClase').addEventlistener('evento', (e) => {

    // Codigo Aqui

});
```

Mas eventos revisar en Pagina [https://developer.mozilla.org/es/docs/Web/Events](https://developer.mozilla.org/es/docs/Web/Events)

