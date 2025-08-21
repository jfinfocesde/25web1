# Actividad 3 - Momento 1

##  Ejercicios con Funciones en JavaScript

!!! info "Introducción"
    Esta actividad está diseñada para reforzar tu comprensión de las funciones en JavaScript. Cada enunciado te pide resolver un problema utilizando un tipo específico de función: **declaración de función**, **expresión de función**, **función flecha**, **función anónima**, **IIFE**, **función recursiva** o **función de orden superior**. Antes de comenzar, sigue las instrucciones para hacer un fork del repositorio donde resolverás la actividad. ¡Practica y domina las funciones! 🚀

---

## 🛠️ Instrucciones para hacer fork del repositorio

Para trabajar en esta actividad, harás un **fork** del repositorio donde se encuentra el proyecto base. Sigue estos pasos:

1. **Accede al repositorio**:
   - Ve al repositorio oficial en GitHub: 
    ```bash
    https://github.com/jfinfocesde/act_web1_s4.git
    ```
   - Asegúrate de tener una cuenta de GitHub activa.

2. **Haz un fork**:
   - En la esquina superior derecha del repositorio, haz clic en el botón **Fork**.
   - Esto creará una copia del repositorio en tu cuenta de GitHub.

3. **Clona tu repositorio**:
   - En tu cuenta de GitHub, abre el repositorio forkeado.
   - Haz clic en el botón **Code** y copia la URL del repositorio (por ejemplo, `https://github.com/tu-usuario/act_web1_s4.git`).
   - En tu terminal, ejecuta:
     ```bash
     git clone https://github.com/tu-usuario/act_web1_s4.git
     ```
   - Navega al directorio clonado:
     ```bash
     cd nombre-repositorio
     ```

## 📋 Instrucciones para la actividad

- Resuelve cada ejercicio utilizando el tipo de función indicado.
- Escribe el código en JavaScript y prueba tus soluciones en una consola o entorno de desarrollo.
- Cada solución debe ser clara, eficiente y seguir las buenas prácticas mencionadas en la guía previa.

---

## 🛠️ Ejercicios

### 1. **Calcular el cuadrado de un número**
- **Tarea**: Crea una función que reciba un número y devuelva su cuadrado.
- **Tipo de función**: Declaración de función
- **Ejemplo**: `cuadrado(4)` → `16`

### 2. **Saludar con nombre por defecto**
- **Tarea**: Crea una función que salude a una persona por su nombre. Si no se proporciona un nombre, usa "Invitado".
- **Tipo de función**: Expresión de función
- **Ejemplo**: `saludar()` → `¡Hola, Invitado!`

### 3. **Sumar elementos de un arreglo**
- **Tarea**: Crea una función que sume todos los números de un arreglo.
- **Tipo de función**: Función flecha
- **Ejemplo**: `sumarArreglo([1, 2, 3])` → `6`

### 4. **Ejecutar un mensaje instantáneamente**
- **Tarea**: Crea una función que imprima "¡Bienvenido!" en la consola al definirse.
- **Tipo de función**: IIFE
- **Ejemplo**: Imprime automáticamente al ejecutarse.

### 5. **Contar vocales en una cadena**
- **Tarea**: Crea una función que cuente las vocales (a, e, i, o, u) en una cadena.
- **Tipo de función**: Función recursiva
- **Ejemplo**: `contarVocales("hola")` → `2`

### 6. **Filtrar números mayores a 10**
- **Tarea**: Crea una función que reciba un arreglo y devuelva solo los números mayores a 10.
- **Tipo de función**: Función de orden superior
- **Ejemplo**: `filtrarMayores([5, 12, 8, 15])` → `[12, 15]`

### 7. **Convertir a mayúsculas**
- **Tarea**: Crea una función que convierta una cadena a mayúsculas.
- **Tipo de función**: Función flecha
- **Ejemplo**: `aMayusculas("javascript")` → `JAVASCRIPT`

### 8. **Temporizador con mensaje**
- **Tarea**: Crea una función que imprima un mensaje después de 3 segundos usando `setTimeout`.
- **Tipo de función**: Función anónima
- **Ejemplo**: Imprime "¡Tiempo terminado!" tras 3 segundos.

### 9. **Crear un contador privado**
- **Tarea**: Crea una función que devuelva otra función para contar incrementos, manteniendo el contador privado.
- **Tipo de función**: IIFE con closure
- **Ejemplo**: `contador()` → `0`, `contador()` → `1`

### 10. **Calcular factorial**
- **Tarea**: Crea una función que calcule el factorial de un número.
- **Tipo de función**: Función recursiva
- **Ejemplo**: `factorial(5)` → `120`

### 11. **Verificar si un número es par**
- **Tarea**: Crea una función que determine si un número es par.
- **Tipo de función**: Declaración de función
- **Ejemplo**: `esPar(4)` → `true`

### 12. **Multiplicar elementos de un arreglo**
- **Tarea**: Crea una función que multiplique todos los números de un arreglo.
- **Tipo de función**: Función de orden superior
- **Ejemplo**: `multiplicarArreglo([2, 3, 4])` → `24`

### 13. **Reemplazar espacios por guiones**
- **Tarea**: Crea una función que reemplace los espacios en una cadena por guiones.
- **Tipo de función**: Expresión de función
- **Ejemplo**: `reemplazarEspacios("Hola Mundo")` → `Hola-Mundo`

### 14. **Generar un ID único**
- **Tarea**: Crea una función que genere un ID único basado en un contador interno.
- **Tipo de función**: IIFE con closure
- **Ejemplo**: `generarId()` → `1`, `generarId()` → `2`

### 15. **Invertir una cadena**
- **Tarea**: Crea una función que invierta una cadena de texto.
- **Tipo de función**: Función recursiva
- **Ejemplo**: `invertir("hola")` → `aloh`

### 16. **Sumar argumentos variables**
- **Tarea**: Crea una función que sume un número variable de argumentos.
- **Tipo de función**: Función flecha con parámetro rest
- **Ejemplo**: `sumar(1, 2, 3, 4)` → `10`

### 17. **Ejecutar operación personalizada**
- **Tarea**: Crea una función que reciba dos números y una función callback para realizar una operación.
- **Tipo de función**: Función de orden superior
- **Ejemplo**: `operacion(5, 3, (a, b) => a * b)` → `15`

### 18. **Validar correo electrónico**
- **Tarea**: Crea una función que valide si una cadena es un correo electrónico básico (contiene @ y .com).
- **Tipo de función**: Declaración de función
- **Ejemplo**: `esCorreo("test@example.com")` → `true`

### 19. **Retrasar ejecución de un mensaje**
- **Tarea**: Crea una función que imprima un mensaje después de un tiempo definido por el usuario.
- **Tipo de función**: Función anónima con `setTimeout`
- **Ejemplo**: `retrasarMensaje("Hola", 2000)` → Imprime "Hola" tras 2 segundos.

### 20. **Calcular promedio de un arreglo**
- **Tarea**: Crea una función que calcule el promedio de un arreglo de números.
- **Tipo de función**: Función flecha
- **Ejemplo**: `promedio([10, 20, 30])` → `20`

---
