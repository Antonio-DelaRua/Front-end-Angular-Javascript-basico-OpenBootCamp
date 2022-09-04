
Crea un archivo JS que contenga las siguientes líneas

- Una variable que contenga la lista de la compra (mínimo 5 elementos)

- Modifica la lista de la compra y añádele "Aceite de Girasol"

- Vuelve a modificar la lista de la compra eliminando "Aceite de Girasol"

- Una lista de tus 3 películas favoritas (objetos con propiedades: titulo, 
director, fecha)

- Una nueva lista que contenga las películas posteriores al 1 de enero de 
2010 (utilizando filter)

- Una nueva lista que contenga los directores de la lista de películas 
original (utilizando map)

- Una nueva lista que contenga los títulos de la lista de películas 
original (utilizando map)

- Una nueva lista que concatene la lista de directores y la lista de los 
títulos (utilizando concat)

- Una nueva lista que concatene la lista de directores y la lista de los 
títulos (utilizando el factor de propagación)
-------------------------------------------------------------------------

const compra = ["Patatas", "Huevos", "Leche", "Fruta", "Agua"]

compra.push("Aceite de Girasol")
compra.pop()

const peliculas = [
    {
        titulo: "El señor de los anillos",
        director: "Peter Jackson",
        fecha: new Date(2009, 6, 20)
    },
    {
        titulo: "Los vengadores",
        director: "Joss Whedon",
        fecha: new Date(2012, 10, 11)
    },
    {
        titulo: "Uno de los nuestros",
        director: "Martin Scorsesse",
        fecha: new Date(1990, 3, 13)
    }
]

const peliculasNuevas = peliculas.filter(pelicula => pelicula.fecha > new Date(2010, 0, 1))

const directores = peliculas.map(pelicula => {
    return pelicula.director
})
const titulos = peliculas.map(pelicula => {
    return pelicula.titulo
})
const directores_titulos = directores.concat(titulos)
const directores_titulos_prop = [...directores, ...titulos]