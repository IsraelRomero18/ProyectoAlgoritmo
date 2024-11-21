   # css.html
  Ejercicios de cadenas con JavasCript y html faciles de realizar 
   <!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Concatenar Nombre y Apellido</title>
    <style>
        body { font-family: Arial, sans-serif; }
        label { margin-right: 10px; }
        button { margin-top: 10px; }
        #resultado { margin-top: 20px; font-weight: bold; }
    </style>
</head>
<body>
    <label for="nombre">Nombre:</label>
    <input type="text" id="nombre"><br><br>

    <label for="apellido">Apellido:</label>
    <input type="text" id="apellido"><br><br>

    <button onclick="concatenar()">Concatenar</button>

    <div id="resultado"></div>

    <script>
        function concatenar() {
            const nombre = document.getElementById("nombre").value;
            const apellido = document.getElementById("apellido").value;
            document.getElementById("resultado").innerText = ${apellido} ${nombre};
        }
    </script>
</body>
</html>
2. Comparar frases
HTML + CSS + JavaScript
html
Copiar código
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Comparar Frases</title>
    <style>
        body { font-family: Arial, sans-serif; }
        label { margin-right: 10px; }
        button { margin-top: 10px; }
        #resultado { margin-top: 20px; font-weight: bold; }
    </style>
</head>
<body>
    <label for="frase1">Frase 1:</label>
    <input type="text" id="frase1"><br><br>

    <label for="frase2">Frase 2:</label>
    <input type="text" id="frase2"><br><br>

    <button onclick="comparar()">Comparar</button>

    <div id="resultado"></div>

    <script>
        function comparar() {
            const frase1 = document.getElementById("frase1").value;
            const frase2 = document.getElementById("frase2").value;

            let resultado;
            if (frase1 === frase2) {
                resultado = "Las frases son iguales.";
            } else if (frase1 > frase2) {
                resultado = "La primera frase es mayor.";
            } else {
                resultado = "La primera frase es menor.";
            }
            document.getElementById("resultado").innerText = resultado;
        }
    </script>
</body>
</html>
3. Crear palabra con espacios
HTML + CSS + JavaScript
html
Copiar código
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Crear Palabra con Espacios</title>
    <style>
        body { font-family: Arial, sans-serif; }
        label { margin-right: 10px; }
        button { margin-top: 10px; }
        #resultado { margin-top: 20px; font-weight: bold; }
    </style>
</head>
<body>
    <label for="palabra">Ingresa una palabra:</label>
    <input type="text" id="palabra"><br><br>

    <button onclick="crearEspacios()">Crear con Espacios</button>

    <div id="resultado"></div>

    <script>
        function crearEspacios() {
            const palabra = document.getElementById("palabra").value;
            let resultado = palabra.split('').join(' ');
            document.getElementById("resultado").innerText = resultado;
        }
    </script>
</body>
</html>
4. Presentar cada carácter con su código ASCII
HTML + CSS + JavaScript
html
Copiar código
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Código ASCII de cada carácter</title>
    <style>
        body { font-family: Arial, sans-serif; }
        label { margin-right: 10px; }
        button { margin-top: 10px; }
        #resultado { margin-top: 20px; font-weight: bold; }
    </style>
</head>
<body>
    <label for="frase">Ingresa una frase:</label>
    <input type="text" id="frase"><br><br>

    <button onclick="mostrarAscii()">Mostrar ASCII</button>

    <div id="resultado"></div>

    <script>
        function mostrarAscii() {
            const frase = document.getElementById("frase").value;
            let resultado = '';
            frase.split('').forEach(char => {
                resultado += Carácter: ${char}, Código ASCII: ${char.charCodeAt(0)}<br>;
            });
            document.getElementById("resultado").innerHTML = resultado;
        }
    </script>
</body>
</html>
5. Invertir una frase
HTML + CSS + JavaScript
html
Copiar código
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Invertir Frase</title>
    <style>
        body { font-family: Arial, sans-serif; }
        label { margin-right: 10px; }
        button { margin-top: 10px; }
        #resultado { margin-top: 20px; font-weight: bold; }
    </style>
</head>
<body>
    <label for="frase">Ingresa una frase:</label>
    <input type="text" id="frase"><br><br>

    <button onclick="invertirFrase()">Invertir Frase</button>

    <div id="resultado"></div>

    <script>
        function invertirFrase() {
            const frase = document.getElementById("frase").value;
            let invertida = frase.split('').reverse().join('');
            document.getElementById("resultado").innerText = invertida;
        }
    </script>
</body>
</html>
