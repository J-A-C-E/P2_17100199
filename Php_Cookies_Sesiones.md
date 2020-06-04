## Php Cookies y Sesiones

### **Definción de Cookies**
Son variables que se almacenan en la computadora del cliente que visita la página web.
La información que se podrá almacenar en una cookie sepre será de tipo cadena de caracteres.

Para crear una cookie usamos setcookie y le damos como argumento el nombre que va a tener la variable y la información que almacenará, también se debe especficar un tiempo de vida de la cookie por cuestiones de seguridad, pasado este tiempo la cookie se elimina.

```php
setcookie ("usr","Javier",time() + 10);

echo $_COOKIE ['usr'];
 }
```

### **Definición de Sesiones**
Son variables que guardan información en el servidor de la página web.
Un ejemplo de su aplicación es cuando un usuario ingresa su nombre y su contraseña, y esta información se almacena en una variable, para que cuando el usuario cambie de páginas se consulte a la variable si ese usuario está permitido.

Para poder crear una sessión se necesita la función session_start().
Esto sirve para que si la sesión no existiía ateriormente la función crea la sesión y le asocia un identificador único. Por otro lado, si la sesión ya existía, la función permite que la página tenga acceso a la información vinculada a la sesión.


```php
session_start();

if(empty($SESSION['count']))
{
    $_SESSION['count']=1;
}else
{
    $_SESSION['count']++;

}
if($_SESSION['count']==10)
{
    unset($_SESSION["count"]);
    session_destroy();
}
```