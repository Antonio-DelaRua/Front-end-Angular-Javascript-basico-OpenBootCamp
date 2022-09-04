
Crea un nuevo archivo JS que contenga una lista con los siguientes elementos:

- Tu nombre (string)

- Tu edad (number)

- ¿Eres desarrollador? (boolean)

- Tu fecha de nacimiento (Date)

- Tu libro favorito (Objeto con propiedades: titulo, autor, fecha, url)

const lista = [
    "Antonio",
    35,
    false,
    new Date(1986, 5, 6),
    { 
        titulo: "El elfo oscuro",
        autor: "R.A Salvatore",
        fecha: new Date(1996, 0, 1),
        url: "https://www.amazon.es/Elfo-Oscuro-Reinos-Olvidados-Dragonlance/dp/8448037243"
    },
];

console.log(lista)