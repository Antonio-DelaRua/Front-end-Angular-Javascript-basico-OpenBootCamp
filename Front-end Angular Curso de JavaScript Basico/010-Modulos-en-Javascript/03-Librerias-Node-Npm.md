
index.js
---------
// Instalar axios para hacer llamadas a servicios externos
import axios from "axios"

axios.get('https://pokeapi.co/api/v2/pokemon/charmander')
    .then(function (response) {
        // handle success
        console.log("Success!!!")
        console.log(response.data)
    })
    .catch(function (error) {
        // handle error
        console.log("Error!!!")
        console.log(error);
    })

package.json
-------------
{
  "name": "video-librerias",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "type": "module",
  "scripts": {
    "start": "node index.js"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "dependencies": {
    "axios": "^0.26.0"
  }
}