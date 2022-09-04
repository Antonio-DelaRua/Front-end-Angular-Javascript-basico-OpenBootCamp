
tipado en JS:  
- tipado inferido: en el momento que nosotros estamos definiendo
una variable, la definimos de forma general.

ventajas: nos da mucho mas libertad a la hora de crear nuestro framework
          codificaremos muchos mas rapido

tipos en JS:

-grupos primitivos: Number, String, Boolean , Null, Undefined

tipo number: var a = 1
tipo String: var str = "string"
tipo boolean: var bool = True/False
tipo Null: var nul = null
tipo Undefined:var und = undefined

grupos objetos.
--------------------------------------------------------------------
//tipos primitivos
--------------------------------------------------------------------
//number
4;

//string
"Hola mundo";
'Hola mundo';
`Hola mundo`;

//booleanos
true;
false;

// nulo y undefined
null;
undefined;

// null, undefined, false, 0  ----> todas son false
if(true){
    console.log("cumple")
}else{
    console.log("no cumple")
}