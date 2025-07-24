# Semana 3: Soluciones - Ejercicios de Ciclos en JavaScript

Esta página contiene las soluciones completas para todos los ejercicios de la actividad práctica de ciclos en JavaScript.

## 📝 Soluciones - Ejercicios con Ciclo `while`

### Ejercicio While 1: Contador Descendente

```javascript
// Ejercicio While 1: Contador Descendente
console.log("=== Contador Descendente ===");

let contador = 20;

while (contador >= 1) {
    console.log(contador);
    contador--;
}

console.log("¡Despegue!");
```

**Explicación**: Utilizamos un ciclo `while` que continúa mientras el contador sea mayor o igual a 1. En cada iteración mostramos el número y lo decrementamos.

---

### Ejercicio While 2: Suma de Números Pares

```javascript
// Ejercicio While 2: Suma de Números Pares
console.log("=== Suma de Números Pares ===");

let numero = 2; // Comenzamos con el primer número par
let suma = 0;
let cantidadPares = 0;

while (numero <= 50) {
    suma += numero;
    cantidadPares++;
    console.log(`Número par: ${numero}, Suma acumulada: ${suma}`);
    numero += 2; // Incrementamos de 2 en 2 para obtener solo pares
}

console.log(`\nResultado final:`);
console.log(`Suma total de números pares: ${suma}`);
console.log(`Cantidad de números pares sumados: ${cantidadPares}`);
```

**Explicación**: Iniciamos con 2 (primer par) y vamos sumando de 2 en 2 hasta llegar a 50, acumulando la suma y contando cuántos números procesamos.

---

### Ejercicio While 3: Validador de Contraseña

```javascript
// Ejercicio While 3: Validador de Contraseña
console.log("=== Validador de Contraseña ===");

let password = "";
let intentosFallidos = 0;
const passwordCorrecta = "admin123";

while (password !== passwordCorrecta) {
    // Simulamos entrada del usuario (en un entorno real usarías prompt())
    password = prompt("Ingresa la contraseña:");
    
    if (password !== passwordCorrecta) {
        intentosFallidos++;
        console.log(`Contraseña incorrecta. Intento fallido #${intentosFallidos}`);
    }
}

console.log(`¡Acceso concedido!`);
console.log(`Intentos fallidos antes del acceso: ${intentosFallidos}`);
```

**Explicación**: El ciclo `while` continúa hasta que se ingrese la contraseña correcta, contando cada intento fallido.

---

### Ejercicio While 4: Generador de Números Aleatorios

```javascript
// Ejercicio While 4: Generador de Números Aleatorios
console.log("=== Generador de Números Aleatorios ===");

let numeroAleatorio = 0;
let cantidadGenerados = 0;

while (numeroAleatorio <= 95) {
    numeroAleatorio = Math.floor(Math.random() * 100) + 1;
    cantidadGenerados++;
    console.log(`Número ${cantidadGenerados}: ${numeroAleatorio}`);
}

console.log(`\nSe generaron ${cantidadGenerados} números hasta obtener uno mayor a 95`);
console.log(`El número final fue: ${numeroAleatorio}`);
```

**Explicación**: Generamos números aleatorios hasta que obtengamos uno mayor a 95, contando cuántos números se generaron en total.

---

### Ejercicio While 5: Calculadora de Factorial

```javascript
// Ejercicio While 5: Calculadora de Factorial
console.log("=== Calculadora de Factorial ===");

function calcularFactorialWhile(n) {
    if (n < 0) {
        return "El factorial no está definido para números negativos";
    }
    
    let factorial = 1;
    let i = 1;
    
    console.log(`Calculando el factorial de ${n}:`);
    console.log(`Paso inicial: factorial = 1`);
    
    while (i <= n) {
        factorial *= i;
        console.log(`Paso ${i}: factorial = factorial * ${i} = ${factorial}`);
        i++;
    }
    
    return factorial;
}

// Ejemplo de uso
let numero = 5;
let resultado = calcularFactorialWhile(numero);
console.log(`\nEl factorial de ${numero} es: ${resultado}`);
```

**Explicación**: Calculamos el factorial multiplicando progresivamente desde 1 hasta n, mostrando cada paso del cálculo.

---

### Ejercicio While 6: Búsqueda en Array

```javascript
// Ejercicio While 6: Búsqueda en Array
console.log("=== Búsqueda en Array ===");

let nombres = ["Ana", "Carlos", "María", "Pedro", "Lucía", "Diego", "Carmen"];
let nombreBuscado = "María";
let indice = 0;
let encontrado = false;
let posicionEncontrada = -1;

console.log(`Buscando "${nombreBuscado}" en el array:`);
console.log(`Array: [${nombres.join(", ")}]`);

while (indice < nombres.length && !encontrado) {
    console.log(`Verificando posición ${indice}: "${nombres[indice]}"`);
    
    if (nombres[indice] === nombreBuscado) {
        encontrado = true;
        posicionEncontrada = indice;
        console.log(`¡Encontrado! "${nombreBuscado}" está en la posición ${indice}`);
    } else {
        console.log(`"${nombres[indice]}" no es el nombre que buscamos`);
    }
    
    indice++;
}

if (!encontrado) {
    console.log(`El nombre "${nombreBuscado}" no se encontró en el array`);
}
```

**Explicación**: Recorremos el array con `while` hasta encontrar el nombre buscado o llegar al final del array.

---

### Ejercicio While 7: Contador de Dígitos

```javascript
// Ejercicio While 7: Contador de Dígitos
console.log("=== Contador de Dígitos ===");

function contarDigitos(numero) {
    // Convertimos a valor absoluto para manejar números negativos
    numero = Math.abs(numero);
    
    // Caso especial para el 0
    if (numero === 0) {
        return 1;
    }
    
    let contador = 0;
    let temp = numero;
    
    console.log(`Contando dígitos de ${numero}:`);
    
    while (temp > 0) {
        temp = Math.floor(temp / 10);
        contador++;
        console.log(`Paso ${contador}: temp = ${temp}, dígitos contados = ${contador}`);
    }
    
    return contador;
}

// Ejemplos de uso
let numeros = [12345, 987, 42, 7, 0, 1000000];

numeros.forEach(num => {
    let digitos = contarDigitos(num);
    console.log(`El número ${num} tiene ${digitos} dígito(s)\n`);
});
```

**Explicación**: Dividimos el número por 10 repetidamente hasta que sea 0, contando cuántas divisiones realizamos.

---

### Ejercicio While 8: Secuencia de Fibonacci

```javascript
// Ejercicio While 8: Secuencia de Fibonacci
console.log("=== Secuencia de Fibonacci ===");

let a = 0, b = 1;
let contador = 0;
let limite = 15;

console.log("Los primeros 15 números de la secuencia de Fibonacci:");

while (contador < limite) {
    if (contador === 0) {
        console.log(`F(${contador + 1}) = ${a}`);
        contador++;
    } else if (contador === 1) {
        console.log(`F(${contador + 1}) = ${b}`);
        contador++;
    } else {
        let siguiente = a + b;
        console.log(`F(${contador + 1}) = ${siguiente} (${a} + ${b})`);
        a = b;
        b = siguiente;
        contador++;
    }
}
```

**Explicación**: Generamos la secuencia de Fibonacci sumando los dos números anteriores, usando `while` para controlar cuántos números generar.

---

### Ejercicio While 9: Juego de Adivinanza Mejorado

```javascript
// Ejercicio While 9: Juego de Adivinanza Mejorado
console.log("=== Juego de Adivinanza Mejorado ===");

function juegoAdivinanza() {
    let numeroSecreto = Math.floor(Math.random() * 50) + 1;
    let adivinanza = 0;
    let intentos = 0;
    let maxIntentos = 7;
    
    console.log("¡Bienvenido al juego de adivinanza!");
    console.log("Adivina el número entre 1 y 50");
    console.log(`Tienes ${maxIntentos} intentos máximo`);
    console.log("Pistas: 'muy alto', 'muy bajo', 'cerca' (diferencia ≤ 5)");
    
    while (adivinanza !== numeroSecreto && intentos < maxIntentos) {
        // En un entorno real, usarías prompt()
        adivinanza = parseInt(prompt(`Intento ${intentos + 1}/${maxIntentos}. Ingresa tu número:`));
        intentos++;
        
        if (adivinanza === numeroSecreto) {
            console.log(`¡Felicidades! Adivinaste el número ${numeroSecreto} en ${intentos} intento(s)`);
        } else {
            let diferencia = Math.abs(adivinanza - numeroSecreto);
            
            if (diferencia <= 5) {
                console.log("¡Cerca! Estás muy cerca del número");
            } else if (adivinanza < numeroSecreto) {
                console.log("Muy bajo. El número es mayor");
            } else {
                console.log("Muy alto. El número es menor");
            }
            
            if (intentos < maxIntentos) {
                console.log(`Te quedan ${maxIntentos - intentos} intento(s)`);
            }
        }
    }
    
    if (adivinanza !== numeroSecreto) {
        console.log(`Game Over. El número era: ${numeroSecreto}`);
    }
}

// Ejecutar el juego
juegoAdivinanza();
```

**Explicación**: Implementamos un juego completo con pistas inteligentes y límite de intentos usando `while`.

---

### Ejercicio While 10: Procesador de Calificaciones

```javascript
// Ejercicio While 10: Procesador de Calificaciones
console.log("=== Procesador de Calificaciones ===");

function procesarCalificaciones() {
    let calificaciones = [];
    let calificacion = 0;
    let suma = 0;
    
    console.log("Ingresa las calificaciones de los estudiantes");
    console.log("Ingresa -1 para terminar");
    
    while (calificacion !== -1) {
        // En un entorno real, usarías prompt()
        calificacion = parseFloat(prompt("Ingresa una calificación (0-100) o -1 para terminar:"));
        
        if (calificacion !== -1) {
            if (calificacion >= 0 && calificacion <= 100) {
                calificaciones.push(calificacion);
                suma += calificacion;
                console.log(`Calificación ${calificaciones.length}: ${calificacion} agregada`);
            } else {
                console.log("Calificación inválida. Debe estar entre 0 y 100");
            }
        }
    }
    
    if (calificaciones.length > 0) {
        let promedio = suma / calificaciones.length;
        let mayor = Math.max(...calificaciones);
        let menor = Math.min(...calificaciones);
        
        console.log("\n=== RESULTADOS ===");
        console.log(`Total de calificaciones procesadas: ${calificaciones.length}`);
        console.log(`Calificaciones: [${calificaciones.join(", ")}]`);
        console.log(`Promedio: ${promedio.toFixed(2)}`);
        console.log(`Calificación más alta: ${mayor}`);
        console.log(`Calificación más baja: ${menor}`);
    } else {
        console.log("No se ingresaron calificaciones válidas");
    }
}

// Ejecutar el procesador
procesarCalificaciones();
```

**Explicación**: Procesamos calificaciones hasta que el usuario ingrese -1, calculando estadísticas al final.

---

## 🔄 Soluciones - Ejercicios con Ciclo `for`

### Ejercicio For 1: Tabla de Multiplicar Completa

```javascript
// Ejercicio For 1: Tabla de Multiplicar Completa
console.log("=== Tablas de Multiplicar del 1 al 10 ===");

for (let tabla = 1; tabla <= 10; tabla++) {
    console.log(`\n--- TABLA DEL ${tabla} ---`);
    
    for (let multiplicador = 1; multiplicador <= 10; multiplicador++) {
        let resultado = tabla * multiplicador;
        console.log(`${tabla} x ${multiplicador} = ${resultado}`);
    }
}

console.log("\n¡Todas las tablas completadas!");
```

**Explicación**: Usamos ciclos `for` anidados: el externo para cada tabla (1-10) y el interno para cada multiplicación (1-10).

---

### Ejercicio For 2: Patrón de Asteriscos

```javascript
// Ejercicio For 2: Patrón de Asteriscos
console.log("=== Patrón de Asteriscos ===");

let altura = 5;

// Primera parte: creciente (1 a 5 asteriscos)
for (let fila = 1; fila <= altura; fila++) {
    let linea = "";
    for (let asterisco = 1; asterisco <= fila; asterisco++) {
        linea += "*";
    }
    console.log(linea);
}

// Segunda parte: decreciente (4 a 1 asteriscos)
for (let fila = altura - 1; fila >= 1; fila--) {
    let linea = "";
    for (let asterisco = 1; asterisco <= fila; asterisco++) {
        linea += "*";
    }
    console.log(linea);
}
```

**Explicación**: Creamos el patrón en dos partes: primero creciente y luego decreciente, usando ciclos `for` anidados.

---

### Ejercicio For 3: Análisis de Array de Números

```javascript
// Ejercicio For 3: Análisis de Array de Números
console.log("=== Análisis de Array de Números ===");

// Generar array de 20 números aleatorios
let numeros = [];
for (let i = 0; i < 20; i++) {
    numeros.push(Math.floor(Math.random() * 100) + 1);
}

console.log("Array generado:", numeros);

// Análisis usando ciclo for
let mayor = numeros[0];
let menor = numeros[0];
let suma = 0;
let pares = 0;
let impares = 0;

for (let i = 0; i < numeros.length; i++) {
    let numero = numeros[i];
    
    // Actualizar mayor y menor
    if (numero > mayor) mayor = numero;
    if (numero < menor) menor = numero;
    
    // Sumar para el promedio
    suma += numero;
    
    // Contar pares e impares
    if (numero % 2 === 0) {
        pares++;
    } else {
        impares++;
    }
    
    console.log(`Posición ${i}: ${numero} (Mayor: ${mayor}, Menor: ${menor}, Suma: ${suma})`);
}

let promedio = suma / numeros.length;

console.log("\n=== RESULTADOS DEL ANÁLISIS ===");
console.log(`Número mayor: ${mayor}`);
console.log(`Número menor: ${menor}`);
console.log(`Suma total: ${suma}`);
console.log(`Promedio: ${promedio.toFixed(2)}`);
console.log(`Números pares: ${pares}`);
console.log(`Números impares: ${impares}`);
```

**Explicación**: Analizamos un array con un solo ciclo `for`, calculando múltiples estadísticas en una sola pasada.

---

### Ejercicio For 4: Generador de Números Primos

```javascript
// Ejercicio For 4: Generador de Números Primos
console.log("=== Números Primos entre 1 y 100 ===");

let numerosPrimos = [];

for (let numero = 2; numero <= 100; numero++) {
    let esPrimo = true;
    
    // Verificar si el número es primo
    for (let divisor = 2; divisor < numero; divisor++) {
        if (numero % divisor === 0) {
            esPrimo = false;
            break; // No necesitamos seguir verificando
        }
    }
    
    if (esPrimo) {
        numerosPrimos.push(numero);
        console.log(`${numero} es primo`);
    }
}

console.log(`\nSe encontraron ${numerosPrimos.length} números primos:`);
console.log(numerosPrimos.join(", "));
```

**Explicación**: Usamos ciclos `for` anidados para verificar cada número: el externo recorre 2-100, el interno verifica si es primo.

---

### Ejercicio For 5: Invertir Cadenas de Texto

```javascript
// Ejercicio For 5: Invertir Cadenas de Texto
console.log("=== Invertir Cadenas de Texto ===");

function invertirCadena(texto) {
    let textoInvertido = "";
    
    console.log(`Invirtiendo: "${texto}"`);
    console.log("Proceso paso a paso:");
    
    for (let i = texto.length - 1; i >= 0; i--) {
        textoInvertido += texto[i];
        console.log(`Paso ${texto.length - i}: Agregando '${texto[i]}' -> "${textoInvertido}"`);
    }
    
    return textoInvertido;
}

// Ejemplos de uso
let frases = [
    "Hola Mundo",
    "JavaScript",
    "Programación",
    "CESDE"
];

for (let i = 0; i < frases.length; i++) {
    let original = frases[i];
    let invertida = invertirCadena(original);
    
    console.log(`\nOriginal: "${original}"`);
    console.log(`Invertida: "${invertida}"`);
    console.log("---");
}
```

**Explicación**: Recorremos la cadena desde el final hacia el inicio usando `for`, construyendo la cadena invertida carácter por carácter.

---

### Ejercicio For 6: Calculadora de Potencias

```javascript
// Ejercicio For 6: Calculadora de Potencias
console.log("=== Calculadora de Potencias ===");

function calcularPotencia(base, exponente) {
    if (exponente === 0) {
        console.log(`${base}^${exponente} = 1 (cualquier número elevado a 0 es 1)`);
        return 1;
    }
    
    let resultado = 1;
    
    console.log(`Calculando ${base}^${exponente}:`);
    console.log(`Paso inicial: resultado = 1`);
    
    for (let i = 1; i <= Math.abs(exponente); i++) {
        resultado *= base;
        console.log(`Paso ${i}: resultado = resultado * ${base} = ${resultado}`);
    }
    
    // Manejar exponentes negativos
    if (exponente < 0) {
        resultado = 1 / resultado;
        console.log(`Exponente negativo: resultado = 1/${resultado * base} = ${resultado}`);
    }
    
    return resultado;
}

// Ejemplos de uso
let ejemplos = [
    {base: 2, exponente: 5},
    {base: 3, exponente: 4},
    {base: 5, exponente: 3},
    {base: 10, exponente: 2}
];

for (let i = 0; i < ejemplos.length; i++) {
    let {base, exponente} = ejemplos[i];
    let resultado = calcularPotencia(base, exponente);
    console.log(`\nResultado final: ${base}^${exponente} = ${resultado}\n`);
}
```

**Explicación**: Calculamos potencias multiplicando la base por sí misma el número de veces indicado por el exponente.

---

### Ejercicio For 7: Matriz de Suma

```javascript
// Ejercicio For 7: Matriz de Suma
console.log("=== Matriz de Suma 5x5 ===");

let matriz = [];

// Crear y llenar la matriz
for (let fila = 0; fila < 5; fila++) {
    matriz[fila] = []; // Inicializar la fila
    
    for (let columna = 0; columna < 5; columna++) {
        matriz[fila][columna] = fila + columna;
    }
}

// Mostrar la matriz formateada
console.log("Matriz donde cada elemento es la suma de sus índices (fila + columna):");
console.log("\n   ", "0", "1", "2", "3", "4"); // Encabezado de columnas

for (let fila = 0; fila < 5; fila++) {
    let lineaTexto = fila + ": ";
    
    for (let columna = 0; columna < 5; columna++) {
        lineaTexto += matriz[fila][columna] + " ";
    }
    
    console.log(lineaTexto);
}

// Mostrar algunos ejemplos de cálculo
console.log("\nEjemplos de cálculo:");
for (let fila = 0; fila < 3; fila++) {
    for (let columna = 0; columna < 3; columna++) {
        console.log(`matriz[${fila}][${columna}] = ${fila} + ${columna} = ${matriz[fila][columna]}`);
    }
}
```

**Explicación**: Creamos una matriz 5x5 usando ciclos `for` anidados, donde cada elemento es la suma de sus índices.

---

### Ejercicio For 8: Contador de Vocales

```javascript
// Ejercicio For 8: Contador de Vocales
console.log("=== Contador de Vocales ===");

function contarVocales(frase) {
    let vocales = {
        'a': 0, 'e': 0, 'i': 0, 'o': 0, 'u': 0,
        'á': 0, 'é': 0, 'í': 0, 'ó': 0, 'ú': 0
    };
    
    let totalVocales = 0;
    
    console.log(`Analizando la frase: "${frase}"`);
    console.log("Proceso carácter por carácter:");
    
    for (let i = 0; i < frase.length; i++) {
        let caracter = frase[i].toLowerCase();
        
        if (vocales.hasOwnProperty(caracter)) {
            vocales[caracter]++;
            totalVocales++;
            console.log(`Posición ${i}: '${frase[i]}' es vocal -> ${caracter}: ${vocales[caracter]}`);
        } else {
            console.log(`Posición ${i}: '${frase[i]}' no es vocal`);
        }
    }
    
    return {vocales, totalVocales};
}

// Ejemplos de uso
let frases = [
    "Hola mundo",
    "JavaScript es genial",
    "Programación en CESDE",
    "Aprendiendo ciclos for"
];

for (let i = 0; i < frases.length; i++) {
    let resultado = contarVocales(frases[i]);
    
    console.log("\n=== RESULTADOS ===");
    console.log(`Total de vocales: ${resultado.totalVocales}`);
    console.log("Conteo por vocal:");
    
    for (let vocal in resultado.vocales) {
        if (resultado.vocales[vocal] > 0) {
            console.log(`  ${vocal}: ${resultado.vocales[vocal]}`);
        }
    }
    console.log("---\n");
}
```

**Explicación**: Recorremos cada carácter de la frase con `for`, verificando si es vocal y contando cada tipo.

---

### Ejercicio For 9: Secuencia Matemática

```javascript
// Ejercicio For 9: Secuencia Matemática
console.log("=== Secuencia Matemática (Potencias de 2) ===");

let secuencia = [];
let suma = 0;

console.log("Generando la secuencia: 2, 4, 8, 16, 32, 64, 128, 256, 512, 1024");
console.log("(Cada término es 2 elevado a la potencia correspondiente)");

for (let i = 1; i <= 10; i++) {
    let termino = Math.pow(2, i); // 2^i
    secuencia.push(termino);
    suma += termino;
    
    console.log(`Término ${i}: 2^${i} = ${termino} (Suma acumulada: ${suma})`);
}

console.log(`\nSecuencia completa: [${secuencia.join(", ")}]`);
console.log(`Suma total de la secuencia: ${suma}`);

// Verificación alternativa sin Math.pow()
console.log("\nVerificación calculando potencias manualmente:");
let verificacion = 2;
for (let i = 1; i <= 10; i++) {
    console.log(`2^${i} = ${verificacion}`);
    if (i < 10) verificacion *= 2; // Preparar para la siguiente potencia
}
```

**Explicación**: Generamos la secuencia de potencias de 2 usando `for`, calculando cada término y la suma total.

---

### Ejercicio For 10: Validador de Palíndromo

```javascript
// Ejercicio For 10: Validador de Palíndromo
console.log("=== Validador de Palíndromo ===");

function esPalindromo(texto) {
    // Limpiar el texto: quitar espacios y convertir a minúsculas
    let textoLimpio = "";
    
    for (let i = 0; i < texto.length; i++) {
        let caracter = texto[i].toLowerCase();
        if (caracter !== ' ') {
            textoLimpio += caracter;
        }
    }
    
    console.log(`Texto original: "${texto}"`);
    console.log(`Texto limpio: "${textoLimpio}"`);
    
    // Verificar si es palíndromo comparando desde ambos extremos
    let longitud = textoLimpio.length;
    let esPalindromoFlag = true;
    
    console.log("Verificando carácter por carácter:");
    
    for (let i = 0; i < Math.floor(longitud / 2); i++) {
        let caracterIzquierda = textoLimpio[i];
        let caracterDerecha = textoLimpio[longitud - 1 - i];
        
        console.log(`Posición ${i} vs ${longitud - 1 - i}: '${caracterIzquierda}' vs '${caracterDerecha}'`);
        
        if (caracterIzquierda !== caracterDerecha) {
            esPalindromoFlag = false;
            console.log("  -> No coinciden, no es palíndromo");
            break;
        } else {
            console.log("  -> Coinciden ✓");
        }
    }
    
    return esPalindromoFlag;
}

// Ejemplos de uso
let palabras = [
    "radar",
    "nivel",
    "anita lava la tina",
    "hola",
    "reconocer",
    "a man a plan a canal panama",
    "javascript"
];

for (let i = 0; i < palabras.length; i++) {
    let palabra = palabras[i];
    let resultado = esPalindromo(palabra);
    
    console.log(`\nResultado: "${palabra}" ${resultado ? "SÍ" : "NO"} es un palíndromo\n`);
    console.log("---");
}
```

**Explicación**: Verificamos si una palabra es palíndromo comparando caracteres desde ambos extremos hacia el centro usando `for`.

---

## 📋 Resumen de Soluciones

### Técnicas Utilizadas en los Ejercicios `while`:

1. **Contadores y decrementos** - Control de iteraciones
2. **Acumuladores** - Suma de valores
3. **Banderas booleanas** - Control de condiciones
4. **Validación de entrada** - Verificación de datos
5. **Generación aleatoria** - Números aleatorios
6. **Búsqueda secuencial** - Encontrar elementos
7. **Manipulación numérica** - Operaciones matemáticas
8. **Secuencias matemáticas** - Fibonacci
9. **Lógica de juegos** - Interactividad
10. **Procesamiento de datos** - Estadísticas

### Técnicas Utilizadas en los Ejercicios `for`:

1. **Ciclos anidados** - Tablas y matrices
2. **Patrones visuales** - Asteriscos y formas
3. **Análisis de arrays** - Estadísticas múltiples
4. **Algoritmos matemáticos** - Números primos
5. **Manipulación de strings** - Inversión de texto
6. **Cálculos iterativos** - Potencias
7. **Estructuras bidimensionales** - Matrices
8. **Conteo de caracteres** - Análisis de texto
9. **Secuencias numéricas** - Progresiones
10. **Algoritmos de verificación** - Palíndromos

!!! success "¡Ejercicios Completados!"
    Todas las soluciones implementan correctamente los ciclos especificados (`while` o `for`) y demuestran diferentes técnicas de programación. Cada solución incluye comentarios explicativos y ejemplos de salida para facilitar la comprensión.