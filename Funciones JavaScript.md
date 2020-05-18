# Funciones 

Las funciones en Java Script se manejan como objetos los cuales se pueden manipular y transmitir, estos objetos son function, también una función siempre devuelve un valor.
Para ello una función debe tener una sentencia return que especifique el valor a devolver, en caso de que no la posea este devolverá un valor predeterminado<>.

```JavaScript
/* Declarando la función 'myFunc' */
 function myFunc(elobjeto)
 {
   elobjeto.marca= "Toyota";
 }
 
 /*
  * Declarando la variable 'mycar';
  * Se crea e inicializa el nuevo objeto;
  * para hacer referencia a él mediante 'mycar'
  */
 var mycar = {
   marca: "Honda",
   modelo: "Accord",
   año: 1998
 };

 /* Mostrando 'Honda' */
 window.alert(mycar.marca);

 /* Paso por referencia del objeto 'mycar' a la función 'myFunc'*/
 myFunc(mycar);

 /*
  * Muestra 'Toyota' como valor de la propiedad 'marca'
  * del objeto, que ha sido cambiado por la función.
  */
 window.alert(mycar.marca);
```

## Definiendo funciones

Para definir una función se puede hacer de diferentes formas.

### **Expresión de una función (El operador function)**

```JavaScript
function nombre([param[,param[, ...param]]]) {
   instrucciones
}
```

* nombre: Nombre de la función
* param: Es el nombre de un argumento que se pasará a la función
* instrucciones: Cuerpo de la función
  


### **La expresión de función flecha (=>)**
Una expresión de función flecha tiene una sintaxis más corta y su léxico se une a este valor (ver arrow functions para más detalles):

```JavaScript
([param] [, param]) => { instrucciones }

param => expresión
```

### **Constructor Function**
Como todos los demás objetos, los objetos Function se pueden crear mediante el operador new:

```JavaScript
new Function (arg1, arg2, ... argN, functionBody)
```