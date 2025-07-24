# Semana 2: Soluciones - Condicionales en JavaScript

Esta página contiene las soluciones completas para todos los ejercicios del taller de condicionales en JavaScript.

## 📝 Soluciones de los Ejercicios

### 1️⃣ Par o Impar

**Archivo:** `src/ejercicio1.js`

```javascript
// Ejercicio 1: Par o Impar
let numero = 7;

if (numero % 2 === 0) {
    console.log("par");
} else {
    console.log("impar");
}

// Salida: impar
```

**Explicación**: Utilizamos el operador módulo (`%`) para verificar si el residuo de la división entre 2 es 0. Si es 0, el número es par; si no, es impar.

---

### 2️⃣ Mayor de dos números

**Archivo:** `src/ejercicio2.js`

```javascript
// Ejercicio 2: Mayor de dos números
let a = 14;
let b = 9;

if (a > b) {
    console.log(a);
} else if (b > a) {
    console.log(b);
} else {
    console.log("Los números son iguales");
}

// Salida: 14
```

**Explicación**: Comparamos los dos números usando `if` y `else if`. También incluimos un caso para cuando los números son iguales.

---

### 3️⃣ Clasificación de edad

**Archivo:** `src/ejercicio3.js`

```javascript
// Ejercicio 3: Clasificación de edad
let edad = 15;

if (edad >= 0 && edad <= 12) {
    console.log("niño");
} else if (edad >= 13 && edad <= 17) {
    console.log("adolescente");
} else if (edad >= 18 && edad <= 64) {
    console.log("adulto");
} else if (edad >= 65) {
    console.log("anciano");
} else {
    console.log("Edad no válida");
}

// Salida: adolescente
```

**Explicación**: Usamos múltiples condiciones `else if` para clasificar la edad en diferentes categorías. Incluimos validación para edades negativas.

---

### 4️⃣ Calculadora básica con switch

**Archivo:** `src/ejercicio4.js`

```javascript
// Ejercicio 4: Calculadora básica con switch
let a = 10;
let b = 3;
let operador = '*';
let resultado;

switch (operador) {
    case '+':
        resultado = a + b;
        console.log(resultado);
        break;
    case '-':
        resultado = a - b;
        console.log(resultado);
        break;
    case '*':
        resultado = a * b;
        console.log(resultado);
        break;
    case '/':
        if (b === 0) {
            console.log("indeterminado");
        } else {
            resultado = a / b;
            console.log(resultado);
        }
        break;
    default:
        console.log("operador no válido");
}

// Salida: 30
```

**Explicación**: Utilizamos `switch` para evaluar el operador y realizar la operación correspondiente. Incluimos validación especial para división por cero.

---

### 5️⃣ Día laborable o fin de semana

**Archivo:** `src/ejercicio5.js`

```javascript
// Ejercicio 5: Día laborable o fin de semana
let dia = 'sabado';

// Convertir a minúsculas para evitar problemas de mayúsculas
dia = dia.toLowerCase();

switch (dia) {
    case 'lunes':
    case 'martes':
    case 'miercoles':
    case 'miércoles':
    case 'jueves':
    case 'viernes':
        console.log("laborable");
        break;
    case 'sabado':
    case 'sábado':
    case 'domingo':
        console.log("fin de semana");
        break;
    default:
        console.log("Día no válido");
}

// Salida: fin de semana
```

**Explicación**: Usamos `switch` con múltiples casos para agrupar los días laborables. Incluimos variaciones con y sin acentos para mayor flexibilidad.

---

### 6️⃣ Nota a letra

**Archivo:** `src/ejercicio6.js`

```javascript
// Ejercicio 6: Nota a letra
let nota = 83;

if (nota >= 90 && nota <= 100) {
    console.log("A");
} else if (nota >= 80 && nota <= 89) {
    console.log("B");
} else if (nota >= 70 && nota <= 79) {
    console.log("C");
} else if (nota >= 60 && nota <= 69) {
    console.log("D");
} else if (nota >= 0 && nota < 60) {
    console.log("F");
} else {
    console.log("Nota no válida");
}

// Salida: B
```

**Explicación**: Utilizamos `else if` para evaluar los rangos de notas. Incluimos validación para notas fuera del rango 0-100.

---

### 7️⃣ Descuento por volumen

**Archivo:** `src/ejercicio7.js`

```javascript
// Ejercicio 7: Descuento por volumen
let precioUnitario = 25;
let cantidad = 60;
let precioFinal;
let total = precioUnitario * cantidad;
let descuento = 0;

if (cantidad < 10) {
    descuento = 0;
} else if (cantidad >= 10 && cantidad < 50) {
    descuento = 0.10; // 10%
} else if (cantidad >= 50) {
    descuento = 0.20; // 20%
}

precioFinal = total - (total * descuento);
precioFinal = Math.round(precioFinal * 100) / 100; // Redondear a 2 decimales

console.log(precioFinal);

// Salida: 1200
```

**Explicación**: Calculamos el total, determinamos el descuento según la cantidad, y aplicamos el descuento. Usamos `Math.round()` para redondear a 2 decimales.

---

### 8️⃣ Transporte con tarifa reducida

**Archivo:** `src/ejercicio8.js`

```javascript
// Ejercicio 8: Transporte con tarifa reducida
let edad = 67;
let distanciaKm = 120;
let tarifaBase = distanciaKm * 0.21;
let descuento = 0;
let precioFinal;

if (edad < 18) {
    descuento = 0.20; // 20% descuento
} else if (edad >= 65) {
    descuento = 0.40; // 40% descuento
} else {
    descuento = 0; // Sin descuento
}

precioFinal = tarifaBase - (tarifaBase * descuento);
precioFinal = Math.round(precioFinal * 100) / 100; // Redondear a 2 decimales

console.log(precioFinal);

// Salida: 15.12
```

**Explicación**: Calculamos la tarifa base, determinamos el descuento según la edad, y aplicamos el descuento correspondiente.

---

### 9️⃣ Conversor de notas musicales (switch)

**Archivo:** `src/ejercicio9.js`

```javascript
// Ejercicio 9: Conversor de notas musicales
let nota = 'LA';

// Convertir a mayúsculas para consistencia
nota = nota.toUpperCase();

switch (nota) {
    case 'DO':
        console.log(60);
        break;
    case 'RE':
        console.log(62);
        break;
    case 'MI':
        console.log(64);
        break;
    case 'FA':
        console.log(65);
        break;
    case 'SOL':
        console.log(67);
        break;
    case 'LA':
        console.log(69);
        break;
    case 'SI':
        console.log(71);
        break;
    default:
        console.log("nota desconocida");
}

// Salida: 69
```

**Explicación**: Utilizamos `switch` para mapear cada nota musical a su número MIDI correspondiente. Convertimos a mayúsculas para evitar problemas de case sensitivity.

---

### 🔟 Autenticación simple

**Archivo:** `src/ejercicio10.js`

```javascript
// Ejercicio 10: Autenticación simple
let usuario = "admin";
let contrasena = "1234";

if (usuario === "admin" && contrasena === "1234") {
    console.log("acceso concedido");
} else {
    console.log("acceso denegado");
}

// Salida: acceso concedido
```

**Explicación**: Utilizamos el operador lógico `&&` para verificar que tanto el usuario como la contraseña sean correctos. Usamos `===` para comparación estricta.

---

## 📋 Resumen de Conceptos Aplicados

### Estructuras Condicionales Utilizadas:

1. **`if` simple** - Para condiciones básicas
2. **`if...else`** - Para alternativas binarias
3. **`if...else if...else`** - Para múltiples condiciones
4. **`switch`** - Para comparaciones exactas con múltiples valores
5. **Operadores lógicos** - `&&`, `||` para combinar condiciones
6. **Operadores de comparación** - `===`, `!==`, `>`, `<`, `>=`, `<=`

### Técnicas de Programación:

- **Validación de datos** - Verificar rangos válidos
- **Manejo de casos especiales** - División por cero, valores inválidos
- **Normalización de entrada** - `toLowerCase()`, `toUpperCase()`
- **Cálculos matemáticos** - Porcentajes, descuentos, redondeo
- **Operador módulo** - Para determinar paridad
- **Redondeo a decimales** - `Math.round()` para precisión

### Buenas Prácticas Implementadas:

1. **Comentarios explicativos** en cada ejercicio
2. **Validación de entrada** para casos edge
3. **Nombres descriptivos** para variables
4. **Manejo de casos por defecto** en `switch`
5. **Uso de `break`** para evitar fall-through
6. **Comparaciones estrictas** con `===`

!!! success "¡Ejercicios Completados!"
    Todas las soluciones implementan correctamente las estructuras condicionales requeridas (`if`, `else`, `else if`, `switch`) sin usar funciones ni ciclos, tal como se especificó en las instrucciones del taller.

!!! tip "Consejos para Mejorar"
    - Practica con diferentes valores de entrada para probar todos los casos
    - Experimenta combinando múltiples condiciones con operadores lógicos
    - Considera la legibilidad del código al elegir entre `if/else if` y `switch`
    - Siempre incluye casos por defecto para manejar entradas inesperadas