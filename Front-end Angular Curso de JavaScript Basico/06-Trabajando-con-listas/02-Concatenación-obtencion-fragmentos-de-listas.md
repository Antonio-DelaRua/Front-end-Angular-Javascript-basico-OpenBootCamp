

IMPORTANTE

// Cómo unir dos listas .concat(lista2)
const lista1 = ["hola", 2, false, null]
const lista2 = ["adiós", 8, true, undefined]

console.log(lista1.concat(lista2))
console.log(lista1)

const lista3 = lista1.concat(lista2)
console.log(lista3)

// Cómo unir dos listas con el factor de propagación
console.log(...lista3)

const lista4 = [...lista1, ...lista2]
console.log(lista4)

// ERROR!! Mal entendido el concepto del factor de propagación
const lista5 = [lista1, lista2]
console.log(lista5)

// Cómo obtener una lista a partir de otra .slice()
const array = ["hola", 1, 2, 3, true, null, "adios"]

// NO MODIFICA EL VALOR DEL ARRAY ORIGINAL
console.log(array.slice(1, 4))
const array2 = array.slice(2, 5)
console.log(array2)

const array3 = array.slice(2, -2)
console.log(array3)