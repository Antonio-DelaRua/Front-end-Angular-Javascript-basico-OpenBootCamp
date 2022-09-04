
//var variable;
//let variablelet;

//const constante;
const constante = "hola soy una constante";

var a = 1;
console.log(a);

a = 4;
console.log(a);

let b = 3;
console.log(b);

b = 5;
console.log(b);

/* la diferencia entre let y var es que let afecta a 
todo el codigo y let solo afecta al bloque donde este siendo 
declarado */

var variable = "hola soy una variable VAR"

for (var i = 0; i < 3; i++){
    var variable = "soy la segunda variable"
}

console.log(variable)

let variablelet = "hola soy una variable VAR"

for (var i = 0; i < 3; i++){
    let variable = "soy la segunda variable"
}

console.log(variablelet);
//----------------------------------------------------------------

// para saber que tipo es nuestra variable
console.log(typeof 1)
console.log(typeof variablelet)

//--------------------------------------------

var num = 4;

console.log(typeof num)

num = "hola soy un num"

console.log(typeof num)