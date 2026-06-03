# 📚 Guía Educativa: Plataforma Juvenil de Participación

## 🎯 ¿Qué es esta aplicación?

Esta es una **plataforma de votación y participación juvenil** creada con propósitos pedagógicos. Es un proyecto educativo que te enseña cómo la tecnología puede apoyar ejercicios de:

- **Participación democrática**: Permite que jóvenes propongan ideas y voten por candidatos
- **Transparencia**: Registra quién vota y por quién (trazabilidad)
- **Control ciudadano**: Permite ver resultados en tiempo real
- **Versionamiento de código**: Usa Git para documentar cada cambio

**⚠️ Importante**: Este es un proyecto académico. No recolecta datos personales reales, no representa una elección oficial y es solo para aprender.

---

## 🚀 ¿Cómo funciona?

### Flujo de la aplicación:

1. **Usuario accede a `votar.html`** → Ve la lista de candidatos
2. **Usuario emite su voto** → Se guarda en `votos.json`
3. **Usuario ve resultados en `tablero-de-resultados.html`** → Gráficos con los votos
4. **Backend (`server.js`)** → Gestiona los datos en el servidor

### Componentes principales:

```
plataforma-juvenil-participacion/
├── votar.html                    → Página para votar
├── tablero-de-resultados.html    → Página de resultados
├── index.html                    → Página inicio
├── app.js                        → Lógica de frontend
├── server.js                     → Servidor Node.js
├── styles.css                    → Estilos CSS
├── package.json                  → Dependencias del proyecto
└── data/
    ├── candidatos.json           → Lista de candidatos
    └── votos.json                → Registro de votos
```

---

## 🛠️ Tecnologías que aprenderás

### 1. **HTML** (HyperText Markup Language)
**¿Qué es?** El lenguaje para crear la estructura de páginas web.

📖 **Dónde está en el proyecto:**
- `votar.html` - Formulario de votación
- `tablero-de-resultados.html` - Tabla de resultados
- `index.html` - Página inicial

**Concepto básico:**
```html
<button id="botónVotar">Votar</button>
<div id="resultado"></div>
```

**¿Qué aprendes?**
- Crear formularios
- Estructurar contenido
- Organizar elementos en la página

**Recursos para aprender:**
- 📺 YouTube: "HTML en 1 hora" (en español)
- 📖 MDN Web Docs: https://developer.mozilla.org/es/docs/Web/HTML
- 🎮 Codecademy: Curso interactivo de HTML

---

### 2. **CSS** (Cascading Style Sheets)
**¿Qué es?** El lenguaje para darle estilo y color a las páginas web.

📖 **Dónde está en el proyecto:**
- `styles.css` - Todos los estilos visuales

**Concepto básico:**
```css
button {
  background-color: blue;
  color: white;
  padding: 10px;
}
```

**¿Qué aprendes?**
- Colores y tipografía
- Layout responsivo (se adapta a móvil/desktop)
- Animaciones básicas

**Recursos para aprender:**
- 📺 YouTube: "CSS en 1 hora"
- 📖 MDN Web Docs: https://developer.mozilla.org/es/docs/Web/CSS
- 🎮 Flexbox Froggy: Juego interactivo para aprender Flexbox

---

### 3. **JavaScript**
**¿Qué es?** El lenguaje de programación que hace que las páginas web sean interactivas.

📖 **Dónde está en el proyecto:**
- `app.js` - Lógica de interacción en el navegador
- `server.js` - Servidor Node.js

**Concepto básico:**
```javascript
// Escuchar clic en botón
document.getElementById('botónVotar').addEventListener('click', function() {
  console.log('¡El usuario votó!');
});
```

**¿Qué aprendes?**
- Variables y funciones
- Manipulación del DOM (modificar HTML dinámicamente)
- Peticiones HTTP (comunicación cliente-servidor)
- Eventos (clics, cambios de entrada)

**Recursos para aprender:**
- 📺 YouTube: "JavaScript desde cero" (30+ horas)
- 📖 MDN Web Docs: https://developer.mozilla.org/es/docs/Web/JavaScript
- 🎮 Codecademy: Curso interactivo

---

### 4. **Node.js**
**¿Qué es?** Un entorno que te permite ejecutar JavaScript en el servidor (no en el navegador).

📖 **Dónde está en el proyecto:**
- `server.js` - Ejecuta el servidor web

**Concepto básico:**
```javascript
const express = require("express");
const app = express();

app.listen(3000, () => {
  console.log('Servidor escuchando en puerto 3000');
});
```

**¿Qué aprendes?**
- Crear servidores web
- Gestionar archivos en el servidor
- API REST (crear endpoints)

**Recursos para aprender:**
- 📺 YouTube: "Node.js para principiantes"
- 📖 Documentación oficial: https://nodejs.org/es/docs/
- 🎮 Codecademy: Node.js Fundamentals

---

### 5. **Express.js**
**¿Qué es?** Una librería de Node.js que facilita crear servidores web.

📖 **Dónde está en el proyecto:**
- `server.js` - Todo el código del servidor usa Express

**Concepto básico:**
```javascript
// GET: Obtener candidatos
app.get("/api/candidatos", (req, res) => {
  res.json(candidatos);
});

// POST: Registrar un voto
app.post("/api/votos", (req, res) => {
  guardarVoto(req.body);
  res.json({ éxito: true });
});
```

**¿Qué aprendes?**
- Crear rutas (endpoints)
- Manejar solicitudes HTTP (GET, POST, PUT, DELETE)
- Responses (respuestas del servidor)

**Recursos para aprender:**
- 📖 Documentación oficial: https://expressjs.com/es/
- 📺 YouTube: "Express.js Tutorial"

---

### 6. **JSON**
**¿Qué es?** Formato de datos para almacenar información estructurada.

📖 **Dónde está en el proyecto:**
- `data/candidatos.json` - Lista de candidatos
- `data/votos.json` - Registro de votos

**Concepto básico:**
```json
{
  "candidatos": [
    {
      "id": 1,
      "nombre": "Juan",
      "rol": "Presidente",
      "propuesta": "Mejorar transporte"
    }
  ]
}
```

**¿Qué aprendes?**
- Estructura de datos
- Arrays y objetos
- Serialización de datos

**Recursos para aprender:**
- 📖 MDN Web Docs: https://developer.mozilla.org/es/docs/Learn/JavaScript/Objects/JSON

---

### 7. **Git & GitHub**
**¿Qué es?** Sistema de versionamiento que registra cada cambio en tu código.

📖 **Dónde está en el proyecto:**
- Cada commit registra un cambio
- Las ramas (`main`, `clase-32-tablero-resultados`) guardan versiones diferentes

**Concepto básico:**
```bash
git add .                  # Preparar cambios
git commit -m "Descripción"  # Guardar cambio
git push                   # Enviar a GitHub
```

**¿Qué aprendes?**
- Registrar cambios del código
- Trabajar en equipo sin conflictos
- Ver el historial completo del proyecto
- Colaboración y transparencia

**Recursos para aprender:**
- 📺 YouTube: "Git y GitHub en 1 hora"
- 📖 Documentación: https://git-scm.com/book/es/v2
- 🎮 GitHub Learning Lab: Cursos interactivos

---

## 🎓 Ruta de aprendizaje recomendada

### Semana 1-2: Fundamentos Frontend
1. Aprende **HTML** (estructura)
2. Aprende **CSS** (estilo)
3. Aprende **JavaScript básico** (interactividad)
4. **Tarea**: Modifica `votar.html` y `styles.css`

### Semana 3-4: JavaScript Avanzado
1. **DOM manipulation** (modificar HTML con JavaScript)
2. **Fetch API** (comunicación con el servidor)
3. **Eventos** (clics, cambios)
4. **Tarea**: Modifica `app.js` para agregar nuevas funcionalidades

### Semana 5-6: Backend con Node.js
1. Aprende **Node.js básico**
2. Aprende **Express.js**
3. Aprende **API REST**
4. **Tarea**: Crea nuevos endpoints en `server.js`

### Semana 7-8: Versionamiento y Colaboración
1. Aprende **Git** (commits, ramas)
2. Aprende **GitHub** (pull requests, issues)
3. **Tarea**: Colabora con compañeros usando ramas de trabajo

---

## ▶️ Cómo ejecutar la aplicación

### Paso 1: Instalar dependencias
```bash
npm install
```

### Paso 2: Iniciar el servidor
```bash
npm start
```

### Paso 3: Abrir en el navegador
```
http://localhost:3000
```

---

## 📝 Desafíos para aprender

### 🟢 Nivel Fácil
1. **Cambiar colores**: Modifica `styles.css` para que los botones sean verdes
2. **Agregar un candidato**: Edita `data/candidatos.json` manualmente
3. **Cambiar textos**: Modifica el HTML en `votar.html`

### 🟡 Nivel Intermedio
1. **Validar formulario**: Usa JavaScript para verificar que todos los campos estén llenos
2. **Mostrar mensaje de éxito**: Cuando un usuario vota, mostrar un mensaje
3. **Contar votos**: Crear una función que cuente cuántos votos tiene cada candidato

### 🔴 Nivel Avanzado
1. **Crear endpoint POST**: Agregar un nuevo endpoint en `server.js` para registrar candidatos
2. **Cargar datos dinámicamente**: Usar `fetch()` para obtener candidatos desde el servidor
3. **Gráficos interactivos**: Crear gráficos con Chart.js o D3.js para mostrar resultados

---

## 🔍 Estructura del código

### `app.js` - Lógica del frontend
```javascript
// Aquí va toda la lógica de interacción:
// - Escuchar clics en botones
// - Enviar votos al servidor
// - Mostrar resultados
```

### `server.js` - Lógica del backend
```javascript
// Aquí va toda la lógica del servidor:
// - GET /api/candidatos → devuelve candidatos
// - POST /api/votos → registra un voto
// - Leer y guardar archivos JSON
```

### `styles.css` - Estilos
```css
/* Colores, tipos de letra, tamaños, diseño responsivo */
```

---

## 💡 Conceptos clave a entender

| Concepto | Descripción | Dónde aprender |
|----------|-------------|-----------------|
| **DOM** | La estructura interactiva de HTML | MDN - DOM |
| **API REST** | Forma de comunicarse cliente-servidor | Express.js docs |
| **Fetch API** | Enviar datos al servidor desde JavaScript | MDN - Fetch |
| **Rutas (Routes)** | URLs que responden del servidor | Express.js docs |
| **JSON** | Formato para guardar datos | MDN - JSON |
| **Middleware** | Código que procesa las solicitudes | Express.js docs |

---

## 🆘 Debugging (Solucionar errores)

### En el navegador (Frontend):
```javascript
// Abre las Developer Tools: F12
// Ve a la pestaña "Console" para ver errores
console.log("Variable:", miVariable);
```

### En Node.js (Backend):
```bash
# Mira los mensajes en la terminal
node server.js
```

---

## 📚 Recursos adicionales

### Libros recomendados:
- "Eloquent JavaScript" (gratis online)
- "You Don't Know JS Yet" (JavaScript profundo)

### Canales de YouTube:
- Traversy Media
- FreeCodeCamp
- Soydalhy (en español)

### Plataformas de práctica:
- Codecademy
- FreeCodeCamp
- Exercism
- LeetCode (algoritmos)

---

## 🎯 Objetivo final del aprendizaje

Al terminar este curso, habrás aprendido:
✅ Crear páginas web interactivas con HTML, CSS, JavaScript
✅ Crear un servidor web con Node.js y Express
✅ Comunicación entre cliente y servidor
✅ Almacenar datos en JSON
✅ Usar Git para versionar código
✅ Trabajar en equipo con GitHub

**Esto te prepara para ser un desarrollador web Full Stack junior** 🚀

---

## 📞 Preguntas frecuentes

**P: ¿Por qué usamos Express y no hacer un servidor simple?**
R: Express facilita crear rutas y manejar solicitudes. Es el estándar en la industria.

**P: ¿Por qué guardamos datos en JSON y no en una base de datos?**
R: JSON es simple para aprender. Luego aprenderás bases de datos como MongoDB o PostgreSQL.

**P: ¿Puedo modificar el proyecto?**
R: ¡Claro! Es un proyecto educativo. Experimenta, rompe cosas, aprende de los errores.

**P: ¿Cuánto tiempo toma aprender todo esto?**
R: 4-8 semanas con dedicación. Depende de tu ritmo y experiencia previa.

---

## 🚀 Próximos pasos

1. Lee esta guía completa
2. Elige un desafío fácil para empezar
3. Experimenta modificando el código
4. Consulta los recursos cuando tengas dudas
5. Haz commits en Git después de cada cambio
6. Pide ayuda en el chat cuando necesites

**¡Bienvenido al mundo del desarrollo web! 🎉**
