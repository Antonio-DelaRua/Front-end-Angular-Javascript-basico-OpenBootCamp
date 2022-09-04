
idex.js
--------
// import { suma, eleva, nombre } from './modulos/matematicas.js'
import * as moduloMatematicas from './modulos/matematicas.js'
import getAutor, { libro } from './modulos/literatura.js'

const sum = moduloMatematicas.suma(4, 12)
console.log(sum)

const potencia = moduloMatematicas.eleva(2, 21)
console.log(potencia)

console.log(moduloMatematicas.nombre)

console.log(getAutor())
console.log(libro)

package.json
------------
{
  "name": "modulos-es6",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "type": "module",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "",
  "license": "ISC"
}

módulos/literatura.js
----------------------
const getAutor = () => {
    return "Miguel de Cervantes"
}

export const libro = "Don Quijote de la Mancha"

export default getAutor