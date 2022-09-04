
index.html
----------
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Drag and Drop</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <div class="seccion">
            <p class="parrafo" draggable="true" id="parrafo-1">1. Primero</p>
            <p class="parrafo" draggable="true" id="parrafo-2">2. Segundo</p>
        </div>
        <div class="seccion">
            <p class="parrafo" draggable="true" id="parrafo-3">3. Tercero</p>
            <p class="parrafo" draggable="true" id="parrafo-4">4. Cuarto</p>
        </div>
        <div class="imagen-fantasma"></div>
    </div>
</body>
<script src="index.js"></script>
</html>



index.js
--------
const parrafos = document.querySelectorAll(".parrafo")
const secciones = document.querySelectorAll(".seccion")

parrafos.forEach(parrafo => {
    parrafo.addEventListener("dragstart", event => {
        console.log("Estoy arrastrando el párrafo: " + parrafo.innerText)
        parrafo.classList.add("dragging")
        event.dataTransfer.setData("id", parrafo.id)
        const elemento_fantasma = document.querySelector(".imagen-fantasma")
        event.dataTransfer.setDragImage(elemento_fantasma, 0, 0)
    })

    parrafo.addEventListener("dragend", () => {
        // console.log("He terminado de arrastrar")
        parrafo.classList.remove("dragging")
    })
})

secciones.forEach(seccion => {
    seccion.addEventListener("dragover", event => {
        event.preventDefault()
        event.dataTransfer.dropEffect = "copy" // copy por defecto
        // console.log("Drag Over")
        //
    })

    seccion.addEventListener("drop", event => {
        console.log("Drop")
        const id_parrafo = event.dataTransfer.getData("id")
        // console.log("Párrafo id: ", id_parrafo)
        const parrafo = document.getElementById(id_parrafo)
        seccion.appendChild(parrafo)
    })
})

style.css
----------
.seccion {
    background-color: darkslategrey;
    padding: 1rem;
    margin: 1rem;
}

.parrafo {
    background-color: white;
    padding: 1rem;
}

.parrafo.dragging {
    opacity: 0.3;
}

.imagen-fantasma {
    width: 300px;
    height: 300px;
    background-color: white;
    position: absolute;
    left: -100vw;
}