# Actividad 1 - Momento 2

## Estructuras de Datos en JavaScript (Arrays y Objetos)

**Repositorio GitHub** → `https://github.com/tu-usuario/estructuras-datos-js`

---

## 📦 Instrucciones rápidas

1. **Fork** → `https://github.com/jfinfocesde/act_web1_s7.git`
2. **Clone**  
   ```bash
   git clone https://github.com/TU-USUARIO/act_web1_s7.git
   cd estructuras-datos-js
   ```
3. **Crea** un archivo `ejercicioX.js` (X = 1-20) dentro de `/src`.  
   **IMPORTANTE**: utiliza arreglos, objetos, métodos de arrays, desestructuración y las técnicas vistas en clase.
4. **Ejecuta** tu archivo:  
   ```bash
   node src/ejercicio1.js
   ```
5. **Commit / Push / PR**  
   ```bash
   git add .
   git commit -m "feat: ejercicio X resuelto"
   git push origin main
   ```

---

## 📁 Estructura del repo

```
estructuras-datos-js/
├── README.md
├── src/
│   ├── ejercicio1.js
│   ├── ejercicio2.js
│   ├── ...
│   └── ejercicio20.js
└── .gitignore
```

---

## 🧩 Ejercicios - Estructuras de Datos

### 1️⃣ Gestión de Inventario Básico
**Archivo:** `src/ejercicio1.js`  
Crea un array de objetos que represente un inventario de productos. Cada producto debe tener: `id`, `nombre`, `precio`, `categoria`, `stock`.  
Declara al menos 5 productos y muestra:
- Todos los productos
- Total de productos en inventario
- Valor total del inventario

---

### 2️⃣ Filtrado de Productos por Categoría
**Archivo:** `src/ejercicio2.js`  
Usando el inventario del ejercicio anterior, utiliza el método `filter()` para:
- Mostrar solo productos de la categoría "Electrónicos"
- Mostrar productos con stock menor a 10
- Mostrar productos con precio mayor a $500

---

### 3️⃣ Transformación de Datos con map()
**Archivo:** `src/ejercicio3.js`  
Crea un array de estudiantes con `nombre`, `edad`, `notas` (array de números).  
Usa `map()` para:
- Crear un nuevo array con solo los nombres
- Crear un array con el promedio de cada estudiante
- Agregar una propiedad `estado` ("Aprobado" si promedio >= 70, "Reprobado" si < 70)

---

### 4️⃣ Análisis de Ventas con reduce()
**Archivo:** `src/ejercicio4.js`  
Dado un array de ventas con `producto`, `cantidad`, `precio`, `fecha`:  
Usa `reduce()` para calcular:
- Total de ingresos
- Producto más vendido (por cantidad)
- Promedio de venta por transacción

---

### 5️⃣ Búsqueda y Verificación
**Archivo:** `src/ejercicio5.js`  
Crea un array de usuarios con `id`, `nombre`, `email`, `activo`.  
Implementa búsquedas usando:
- `find()` para buscar usuario por email
- `findIndex()` para obtener posición de usuario por id
- `some()` para verificar si hay usuarios inactivos
- `every()` para verificar si todos tienen email válido (contiene @)

---

### 6️⃣ Manipulación de Arrays
**Archivo:** `src/ejercicio6.js`  
Crea un array inicial `[1, 2, 3, 4, 5]` y demuestra:
- `push()` y `pop()` - agregar y quitar del final
- `shift()` y `unshift()` - agregar y quitar del inicio
- `splice()` - insertar elementos en posición específica
- `slice()` - extraer porción sin modificar original

---

### 7️⃣ Ordenamiento y Reversión
**Archivo:** `src/ejercicio7.js`  
Crea arrays de:
- Números desordenados - ordena ascendente y descendente
- Nombres de personas - ordena alfabéticamente
- Objetos con propiedad `edad` - ordena por edad
- Usa `reverse()` para invertir el orden

---

### 8️⃣ Desestructuración de Arrays
**Archivo:** `src/ejercicio8.js`  
Dado el array `['JavaScript', 'Python', 'Java', 'C++', 'Go']`:  
- Extrae los primeros 3 lenguajes
- Extrae el primero y el último
- Usa rest operator para separar el primero del resto
- Intercambia dos variables usando desestructuración

---

### 9️⃣ Desestructuración de Objetos
**Archivo:** `src/ejercicio9.js`  
Crea un objeto `persona` con propiedades anidadas (dirección, contacto).  
Demuestra:
- Desestructuración básica
- Renombrado de variables
- Valores por defecto
- Desestructuración anidada
- Rest operator en objetos

---

### 🔟 Métodos de Objeto
**Archivo:** `src/ejercicio10.js`  
Crea un objeto y demuestra:
- `Object.keys()` - obtener claves
- `Object.values()` - obtener valores
- `Object.entries()` - obtener pares clave-valor
- Iterar sobre el objeto con `forEach()`

---

### 1️⃣1️⃣ Combinación de Objetos
**Archivo:** `src/ejercicio11.js`  
Crea múltiples objetos y demuestra:
- `Object.assign()` para combinar objetos
- Spread operator para clonar y combinar
- Sobrescritura de propiedades
- Clonación profunda vs superficial

---

### 1️⃣2️⃣ Sistema de Calificaciones
**Archivo:** `src/ejercicio12.js`  
Crea un sistema que:
- Almacene estudiantes con múltiples materias y notas
- Calcule promedio por materia y general
- Identifique estudiantes en riesgo (promedio < 60)
- Use `filter()`, `map()`, `reduce()` combinados

---

### 1️⃣3️⃣ Carrito de Compras Avanzado
**Archivo:** `src/ejercicio13.js`  
Implementa un carrito que:
- Agregue productos (si existe, incremente cantidad)
- Remueva productos completamente
- Actualice cantidades
- Calcule subtotales, impuestos (16%) y total
- Aplique descuentos por cantidad

---

### 1️⃣4️⃣ Procesamiento de Datos CSV
**Archivo:** `src/ejercicio14.js`  
Simula datos CSV como string y:
- Convierte a array de objetos usando `split()` y `map()`
- Filtra registros por criterios específicos
- Agrupa datos por categoría usando `reduce()`
- Genera reporte estadístico

---

### 1️⃣5️⃣ Métodos Avanzados de Arrays
**Archivo:** `src/ejercicio15.js`  
Demuestra:
- `flat()` con arrays anidados
- `flatMap()` para transformar y aplanar
- `Array.from()` para crear arrays desde iterables
- `Array.of()` para crear arrays con elementos específicos

---

### 1️⃣6️⃣ Validación de Formulario
**Archivo:** `src/ejercicio16.js`  
Crea un sistema de validación que:
- Use `every()` para verificar que todos los campos son válidos
- Use `some()` para detectar errores
- Implemente reglas de validación con funciones
- Genere mensajes de error específicos

---

### 1️⃣7️⃣ Análisis de Texto
**Archivo:** `src/ejercicio17.js`  
Dado un texto largo:
- Convierte a array de palabras
- Cuenta frecuencia de cada palabra usando `reduce()`
- Encuentra palabras más comunes
- Filtra palabras por longitud
- Calcula estadísticas del texto

---

### 1️⃣8️⃣ Gestión de Empleados
**Archivo:** `src/ejercicio18.js`  
Crea un sistema que:
- Almacene empleados con departamento, salario, fecha de ingreso
- Agrupe empleados por departamento
- Calcule salario promedio por departamento
- Identifique empleados con mayor antigüedad
- Genere reporte de nómina

---

### 1️⃣9️⃣ Manipulación de Fechas y Arrays
**Archivo:** `src/ejercicio19.js`  
Crea un array de eventos con fechas y:
- Ordena eventos cronológicamente
- Filtra eventos del mes actual
- Agrupa eventos por mes
- Calcula días entre eventos
- Encuentra próximo evento

---

### 2️⃣0️⃣ Proyecto Integrador: Dashboard de Datos
**Archivo:** `src/ejercicio20.js`  
Crea un dashboard que combine todo lo aprendido:
- Múltiples fuentes de datos (usuarios, productos, ventas)
- Métricas calculadas con `reduce()`
- Filtros dinámicos con `filter()`
- Transformaciones con `map()`
- Búsquedas con `find()`
- Validaciones con `every()` y `some()`
- Desestructuración para extraer datos
- Objetos para organizar resultados

---