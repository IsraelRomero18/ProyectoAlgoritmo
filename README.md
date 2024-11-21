   # ejercicios-de-cadenas.html
  Ejercicios de cadenas con JavasCript y html faciles de realizar 
   // Generar un arreglo de 10 números aleatorios entre 1 y 100
    let numeros = Array.from({ length: 10 }, () => Math.floor(Math.random() * 100) + 1);
// Recorrer y mostrar cada número
numeros.forEach((numero, index) => {
    console.log(Número ${index + 1}: ${numero});
});
Promedio de calificaciones: Calcular el promedio de cinco calificaciones ingresadas por el usuario.


// Importar readline para recibir datos del usuario en la terminal
const readline = require('readline');

// Configuración de la interfaz de entrada y salida
const rl = readline.createInterface({
    input: process.stdin,
    output: process.stdout
});

let calificaciones = []; // Arreglo para almacenar las calificaciones
let total = 0;

// Función para pedir las calificaciones al usuario
function pedirCalificaciones(i) {
    if (i < 5) {
        rl.question(`Ingresa la calificación ${i + 1}: `, (respuesta) => {
            let calificacion = parseFloat(respuesta);
            if (!isNaN(calificacion) && calificacion >= 0 && calificacion <= 100) {
                calificaciones.push(calificacion);
                total += calificacion;
                pedirCalificaciones(i + 1); // Pedir la siguiente calificación
            } else {
                console.log("Por favor, ingresa un número válido entre 0 y 100.");
                pedirCalificaciones(i); // Repetir la entrada para esta calificación
            }
        });
    } else {
        // Calcular el promedio
        let promedio = total / calificaciones.length;
        console.log(Las calificaciones ingresadas son: ${calificaciones.join(", ")});
        console.log(El promedio de las calificaciones es: ${promedio.toFixed(2)});
        rl.close(); // Cerrar la interfaz
    }
}

// Iniciar el programa
pedirCalificaciones(0);
