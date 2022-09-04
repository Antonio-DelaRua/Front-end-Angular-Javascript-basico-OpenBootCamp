
Crea un archivo llamado objetos.js que contenga las siguientes líneas

- Un objeto con tus datos personales (nombre, apellido, edad, altura, 
eresDesarrollador)

- Una variable que obtenga tu edad a partir del objeto anterior

- Una lista que contenga el objeto con tus datos personales y un nuevo 
objeto con los datos personales de tus dos mejores amig@s

- Una nueva lista con los objetos de la lista anterior ordenados por edad, 
de mayor a menor
-------------------------------------------------------------------------
const datos = {
    nombre: "Antonio",
    apellido: "DelaRua",
    edad: 35,
    altura: 182,
    eresDesarrollador: false
}

const edad = datos.edad
const lista = [
    {
        ...datos
    },{
        nombre: "Juan",
        apellido: "Aranzadi",
        edad: 34,
        altura: 172,
        eresDesarrollador: false
    },{
        nombre: "Daniel",
        apellido: "Urbano",
        edad: 39,
        altura: 191,
        eresDesarrollador: true
    }
]

const listaOrdenada = lista.sort((a, b) => b.edad - a.edad)

console.log(listaOrdenada)
