# ACTIVIDAD-7-PARALLAX
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>Parallax</title>

<style>
body {
    margin: 0;
    height: 200vh;
    overflow-x: hidden;
    background: black;
}

.parallax {
    position: fixed;
    width: 100%;
    height: 100%;
    overflow: hidden;
}

.layer {
    position: absolute;
    width: 100%;
    height: 100%;
    object-fit: cover;
}

/* Orden Z (fondo → frente) */
#fondo { z-index: 1; }
#nube { z-index: 2; }
#m2 { z-index: 3; }
#m3 { z-index: 4; }
#big { z-index: 5; }
#fog { z-index: 6; }
#m5 { z-index: 7; }
#land { z-index: 8; }
#puente { z-index: 9; }

</style>
</head>

<body>

<div class="parallax">
    <img src="IMG-FONDO.png" class="layer" id="fondo">
    <img src="IMG-NUBE.png" class="layer" id="nube">
    <img src="IMG-MOUNTAIN-2.png" class="layer" id="m2">
    <img src="IMG-MOUNTAIN-3.png" class="layer" id="m3">
    <img src="IMG-4BIG-MOUNTAIN.png" class="layer" id="big">
    <img src="FOG.png" class="layer" id="fog">
    <img src="IMG-MOUNTAIN-5.png" class="layer" id="m5">
    <img src="IMG-LAND.png" class="layer" id="land">
    <img src="IMG-MONTAÑA-CON-PUENTE.png" class="layer" id="puente">
</div>

<script>
let fondo = document.getElementById("fondo");
let nube = document.getElementById("nube");
let m2 = document.getElementById("m2");
let m3 = document.getElementById("m3");
let big = document.getElementById("big");
let fog = document.getElementById("fog");
let m5 = document.getElementById("m5");
let land = document.getElementById("land");
let puente = document.getElementById("puente");

window.addEventListener("scroll", function() {
    let value = window.scrollY;

    fondo.style.transform = `translateY(${value * 0.1}px)`;
    nube.style.transform = `translateY(${value * 0.2}px)`;
    m2.style.transform = `translateY(${value * 0.3}px)`;
    m3.style.transform = `translateY(${value * 0.4}px)`;
    big.style.transform = `translateY(${value * 0.5}px)`;
    fog.style.transform = `translateY(${value * 0.6}px)`;
    m5.style.transform = `translateY(${value * 0.7}px)`;
    land.style.transform = `translateY(${value * 0.85}px)`;
    puente.style.transform = `translateY(${value * 1}px)`;
});
</script>

</body>
</html>
