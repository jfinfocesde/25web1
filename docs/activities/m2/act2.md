# Actividad 2 - Momento 2

## Manipulación del DOM en JavaScript

---

## 📦 Instrucciones rápidas

1. **Fork** → `https://github.com/jfinfocesde/act_web1_s9.git`
2. **Clone**  
   ```bash
   git clone https://github.com/TU-USUARIO/act_web1_s9.git
   cd act_web1_s9
   ```
3. **Crea** un archivo `ejercicioX.html` y `ejercicioX.js` (X = 1-10) dentro de `/src`.  
   **IMPORTANTE**: utiliza selectores del DOM, navegación por nodos, manipulación de elementos y las técnicas vistas en clase.

---

## 📁 Estructura del repo

```
dom-manipulation-js/
├── README.md
├── src/
│   ├── ejercicio1.html
│   ├── ejercicio1.js
│   ├── ejercicio2.html
│   ├── ejercicio2.js
│   ├── ...
│   ├── ejercicio10.html
│   └── ejercicio10.js
├── assets/
│   ├── css/
│   │   └── styles.css
│   └── images/
└── .gitignore
```

---

## 🧩 Ejercicios - Manipulación del DOM

### 1️⃣ Información Básica del Documento
**Archivos:** `src/ejercicio1.html` y `src/ejercicio1.js`  
Crea una página HTML simple que muestre:  

- Título de la página usando `document.title`
- URL actual usando `document.URL`
- Mostrar esta información en un div en la página

---

### 2️⃣ Seleccionar Elementos por ID
**Archivos:** `src/ejercicio2.html` y `src/ejercicio2.js`  
Crea una página con varios elementos que tengan ID y:  

- Usa `getElementById()` para seleccionar elementos
- Cambia el texto de los elementos seleccionados
- Cambia el color de fondo de un elemento

---

### 3️⃣ Seleccionar Elementos por Clase
**Archivos:** `src/ejercicio3.html` y `src/ejercicio3.js`  
Crea elementos con la misma clase y:  

- Usa `getElementsByClassName()` para seleccionarlos
- Cambia el estilo de todos los elementos de esa clase
- Cuenta cuántos elementos tienen esa clase

---

### 4️⃣ Cambiar Contenido de Elementos
**Archivos:** `src/ejercicio4.html` y `src/ejercicio4.js`  
Crea elementos con texto y:  

- Usa `textContent` para cambiar el texto
- Usa `innerHTML` para agregar HTML
- Crea un botón que cambie el contenido al hacer clic

---

### 5️⃣ Modificar Atributos
**Archivos:** `src/ejercicio5.html` y `src/ejercicio5.js`  
Crea elementos con atributos y:  

- Usa `getAttribute()` para leer atributos
- Usa `setAttribute()` para cambiar atributos
- Cambia el src de una imagen y el href de un enlace

---

### 6️⃣ Agregar y Quitar Clases CSS
**Archivos:** `src/ejercicio6.html` y `src/ejercicio6.js`  
Crea elementos con estilos CSS y:  

- Usa `classList.add()` para agregar clases
- Usa `classList.remove()` para quitar clases
- Usa `classList.toggle()` para alternar clases

---

### 7️⃣ Crear y Agregar Elementos
**Archivos:** `src/ejercicio7.html` y `src/ejercicio7.js`  
Crea nuevos elementos dinámicamente:  

- Usa `createElement()` para crear elementos
- Usa `appendChild()` para agregarlos al DOM
- Crea una lista de elementos con un botón

---

### 8️⃣ Eventos Básicos
**Archivos:** `src/ejercicio8.html` y `src/ejercicio8.js`  
Crea elementos interactivos:  

- Usa `addEventListener()` para eventos de click
- Maneja eventos de mouseover y mouseout
- Cambia elementos cuando ocurran los eventos

---

### 9️⃣ Formularios y Validación Simple
**Archivos:** `src/ejercicio9.html` y `src/ejercicio9.js`  
Crea un formulario simple y:  

- Obtén valores de inputs con `value`
- Valida que los campos no estén vacíos
- Muestra mensajes de error o éxito

---

### 🔟 Navegación entre Elementos
**Archivos:** `src/ejercicio10.html` y `src/ejercicio10.js`  
Crea una estructura HTML y demuestra:  

- Usa `parentElement` para acceder al elemento padre
- Usa `children` para acceder a elementos hijos
- Usa `nextElementSibling` para el siguiente hermano
- Muestra la información de navegación en la página

---
