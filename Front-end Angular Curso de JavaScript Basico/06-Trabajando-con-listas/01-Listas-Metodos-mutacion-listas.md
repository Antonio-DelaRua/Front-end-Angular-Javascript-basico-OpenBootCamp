
// como trabajar con listas ( arrays, arreglos, vectores..)
  //let array =[1,2,3,4,5,6]

let array = [1,"hola", false, {id: 5}, null, undefined]

console.log(array)

// acceder a los valores del array a traves de su posicion

console.log(array[0])
console.log(array[1])
console.log(array[2])
console.log(array[3])
console.log(array[4])
console.log(array[5])

// metodos para introducir nuevos valores en nuestros arrays
// .push()  .unshift() => Mutan el valor de nuestro array

// .push sirve para poner valores al final ( puede poner todo tipo 
//de items separados por comas)
array.push("final",45,false)
console.log(array)

// .unshift para introducir nuevos valores al principio
array.unshift("inicio",87,99)
console.log(array)

//metodos para eliminar valores en nuestros arrays
// .pop()  .shift()  => Mutan el valor del array
const array2 = [1, 3, "hola", false]
// .pop() valores al final
array2.pop()
console.log(array2)
array2.pop()
console.log(array2)

// .shift valores al principio
array2.shift()
console.log(array2)
array2.shift()
console.log(array2)

// Metodo para eliminar, modificar o añadir valores en nuestro array
// .splice(x, y, z)
const array3 = [1,2,3,4,5,6]


//eliminar valores .splice(indice, numValoresaEliminar)
array3.splice(2, 1)
console.log(array3)  
array3.splice(2, 3)
console.log(array3)

// añadir valores .splice, 0, valores)
array3.splice(2, 0, "hola")
console.log(array3)
array3.splice(1, 0 , 31)
console.log(array3)

// modificar valores (indice, 1, valor)
array3.splice(2, 1, 3)
console.log(array3)
array3.splice(1, 1, 3, 4)
console.log(array3)