# Trabajo Práctico de Informática III
## Descripción General

Utilizar la biblioteca Three.js (o similar) para crear estos modelos de autos simplificados. Estas imágenes corresponden a modelos que están en diferentes formatos digitales. La idea no es que compren dichas imágenes, sino que vayan construyendo estos modelos con las primitivas Three.js

## Objetivos:

* Generar una página que permita la presentación de un autito similar al de la figura.
* Proporcionar herramientas (a través de teclas o helpers) para modificar las siguientes características:
	* Rotación del autito
	* Cambios de iluminación
	* Alejamiento y acercamiento de la cámara
	* Modificación de las propiedades del material (chapería). Que incluye color, reflectividad, etc.

---
Los componentes de la iluminación, tanto color como intensidad y la posición fueron extraídos del material proveído por el profesor dentro del Three.js Fundamentals, específicamente el material de lección: [threejs-lights-directional](https://threejsfundamentals.org/threejs/lessons/threejs-lights.html), del cual se hace uso de la GUI presente ([dat.GUI](https://github.com/dataarts/dat.gui)) la cual se extiende para los diferentes requisitos del trabajo, y para el cual debemos destacar que cuenta con un issue abierto en su repositorio: [Cannot update NumberControllerBox with .listen() #179.](https://github.com/dataarts/dat.gui/issues/179)

Este error de la GUI no permite que podamos actualizar los números una vez que modificamos el object asociado al mismo, al menos si puede editarse (y mostrarse) el control deslizante o slider como menciona en el issue.

El eje seleccionado para la rotación del auto es el Y debido a que intuitivamente resulta el más conveniente para la perspectiva del mismo y del plano de superficie en que se encuentra. Es posible a través de la GUI realizar un giro de 360° o 6.28 rads.

Escogimos el MeshPhysicalMaterial para casi todo el auto, salvo para los faros, señaleros, radiador, guardabarros, cerraduras y tazas de la ruedas, en el que utilizamos el MeshPhongMaterial con intención que estos se destaquen del resto al no poder ser modificados en la GUI, por decisión propia. Hemos escogido dividir en 4 piezas modificables el auto: carrocería, ruedas, capo y ventanas, de los que podemos variar sus atributos relacionados al tipo de material: opacity, clearcoat, clearcoatRoughness, roughness y metalness. 

Al capo lo inicializamos con opacidad en 0 para visualizar un textura que le agregamos a una capa que se encuentra mínimamente por debajo, al aumentar la opacidad de este módulo o pieza se comporta igual que el resto del auto.

Por diversión colocamos un personaje dentro del auto, no representa nada en absoluto.

---
## Attributions
* Car motor lid texture

![Abstract background with metal textures](https://github.com/Cristobal961/info3Auto/blob/main/images/texture-car.jpg "Abstract background with metal textures")

<a href="https://www.freepik.com/photos/background">Background photo created by kjpargeter - www.freepik.com</a>

* Ugandan Knuckles model and texture

![Ugandan Knuckles](https://github.com/Cristobal961/info3Auto/blob/main/images/knuckles.png "Ugandan Knuckles Model")

<div class="sketchfab-embed-wrapper">
<a href="https://sketchfab.com/3d-models/ugandan-knuckles-d6d71193eaf7498e81d84ec10eb2b576?utm_medium=embed&utm_source=website&utm_campaign=share-popup" target="_blank" style="font-weight: bold; color: #1CAAD9;">Ugandan Knuckles</a>
by <a href="https://sketchfab.com/wardd?utm_medium=embed&utm_source=website&utm_campaign=share-popup" target="_blank" style="font-weight: bold; color: #1CAAD9;">wardd</a>
on <a href="https://sketchfab.com?utm_medium=embed&utm_source=website&utm_campaign=share-popup" target="_blank" style="font-weight: bold; color: #1CAAD9;">Sketchfab</a>
</p>
</div>

