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
document.querySelector('nombreClase').addEventListener('evento', (e) => {

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

###### Recorrer todos los elementos
```javascript
 const elementos = document.querySelectorAll('.c-lightbox');

 elementos.forEach((element) => {
    element.classList.remove('is-show');
 });
```

## Funciones de ayuda


###### RUT
```javascript
function validateRut(campo) {
  if (campo.length == 0) {
    return false;
  }
  if (campo.length < 8) {
    return false;
  }

  campo = campo.replace("-", "");
  campo = campo.replace(/\./g, "");

  var suma = 0;
  var caracteres = "1234567890kK";
  var contador = 0;
  for (var i = 0; i < campo.length; i++) {
    var u = campo.substring(i, i + 1);
    if (caracteres.indexOf(u) != -1) contador++;
  }
  if (contador == 0) {
    return false;
  }

  var rut = campo.substring(0, campo.length - 1);
  var drut = campo.substring(campo.length - 1);
  var dvr = "0";
  var mul = 2;

  for (i = rut.length - 1; i >= 0; i--) {
    suma = suma + rut.charAt(i) * mul;
    if (mul == 7) mul = 2;
    else mul++;
  }
  var res = suma % 11;
  if (res == 1) dvr = "k";
  else if (res == 0) dvr = "0";
  else {
    var dvi = 11 - res;
    dvr = dvi + "";
  }
  if (dvr != drut.toLowerCase()) {
    return false;
  } else {
    return true;
  }
}
```
###### Numero
```javascript
function validateNumber(number) {
  var regex = /^[0-9\-]+$/i;
  return regex.test(number);
}
```

###### Telefono
```javascript
function validatePhone(phone) {
  
  var regex = /([+56]{3})(\d{9})/;
  var regexPhone = /(\d{9})/;

  if (regex.test(phone) || regexPhone.test(phone)) {
    if (phone.length == 12 || phone.length == 9) {
      return true;
    } else {
      return false;
    }
  }
  return false;
}

```
###### Buscar Contenido en un listado
```javascript
 const elementos = document.querySelectorAll('.faq');

 elementos.forEach((element) => {
    
	console.log(element.querySelector('.pregunta').textContent);
	console.log(element.querySelector('.respuesta').innerHTML);
	
 });
```
