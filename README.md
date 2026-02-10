<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Mi San Valentín</title>

<style>
body {
    margin: 0;
    padding: 0;
    overflow: hidden;
    font-family: 'Georgia', serif;
    background: linear-gradient(to bottom, #ffd1dc, #fff0f5);
    text-align: center;
}

.carta {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    background: rgba(255, 255, 255, 0.9);
    padding: 40px;
    border-radius: 20px;
    box-shadow: 0 10px 30px rgba(0,0,0,0.2);
    max-width: 400px;
}

h1 {
    color: #d63384;
}

button {
    margin: 10px;
    padding: 10px 20px;
    border: none;
    border-radius: 20px;
    font-size: 16px;
    cursor: pointer;
}

.si {
    background-color: #ff4d6d;
    color: white;
}

.no {
    background-color: #6c757d;
    color: white;
}

.petalo {
    position: absolute;
    width: 15px;
    height: 15px;
    background: pink;
    border-radius: 50%;
    opacity: 0.8;
    animation: caer linear infinite;
}

@keyframes caer {
    0% {
        transform: translateY(-10px) rotate(0deg);
    }
    100% {
        transform: translateY(100vh) rotate(360deg);
    }
}
</style>
</head>

<body>

<div class="carta">
    <h1>Mi amor 🌸</h1>
    <p>
        Desde que llegaste a mi vida, todo floreció como un cerezo en primavera.
        Cada día contigo es un regalo lleno de amor, paz y felicidad.
    </p>
    <h2>¿Quieres ser mi Valentine? 💝</h2>
    <button class="si" onclick="respuestaSi()">Sí</button>
    <button class="no" onclick="respuestaNo()">No</button>
</div>

<script>
function crearPetalos() {
    for (let i = 0; i < 30; i++) {
        let petalo = document.createElement("div");
        petalo.classList.add("petalo");
        petalo.style.left = Math.random() * 100 + "vw";
        petalo.style.animationDuration = (5 + Math.random() * 5) + "s";
        petalo.style.opacity = Math.random();
        document.body.appendChild(petalo);
    }
}

function respuestaSi() {
    alert("Sabía que dirías que sí ❤️🌸 Te amo muchísimo.");
}

function respuestaNo() {
    alert("Hmm… intenta otra vez 😜💕");
}

crearPetalos();
</script>

</body>
</html>
