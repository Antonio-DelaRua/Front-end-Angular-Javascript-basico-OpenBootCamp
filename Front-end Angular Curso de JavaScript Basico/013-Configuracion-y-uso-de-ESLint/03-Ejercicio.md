
Crea un nuevo proyecto de Node

- Instala la dependencia HTTP Server en entorno global 
(https://www.npmjs.com/package/http-server)

- Crea un fichero index.html (utiliza el comando "!")

- Crea un fichero index.js

- Integra el fichero index.js en el html

- Crea un botón en html (<button>Botón</button>)

- Vincula un evento de tipo "click" al botón anterior, que muestre una alerta en 
el navegador "click en el botón"

- Crea un script para lanzar un servidor de desarrollo con http-server

- Lanza el servidor de desarrollo a través del script anterior y prueba que el 
botón funciona correctamente

- Integra jQuery a través del CDN (https://releases.jquery.com/)

- En el fichero index.js crea un evento click en el botón a través de jQuery, 
que muestre por consola "Hola, estoy utilizando jQuery"


index.html
----------
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sesión 14 - Interacción con HTML</title>
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
</head>
<body>
    <button>Botón</button>
</body>
<script src="index.js"></script>
</html>


index.js
--------
let boton = document.querySelector("button")

boton.addEventListener("click", () => alert("click en el botón"))

$("button").click(function() {
    console.log("Hola, estoy utilizando jQuery")
})


package.json
------------
{
  "name": "14-interaccion-con-html",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "dev": "http-server .",
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "",
  "license": "ISC"
}