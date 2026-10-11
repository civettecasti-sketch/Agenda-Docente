# 🎓 Agenda Docente Profesional

Dashboard web moderno, minimalista y motivador para docentes. Gestiona todo tu año escolar: instituciones, materias, horarios, alumnado, calificaciones, planeación, evaluaciones, familias y bienestar personal.

## 🚀 Características

- ✅ Autenticación con Google (Firebase Auth)
- ✅ Modo local alternativo (sin cuenta)
- ✅ Sincronización en la nube con Firestore
- ✅ Diseño minimalista, formal y motivador
- ✅ Responsive (desktop, tablet, móvil)
- ✅ Modo claro/oscuro
- ✅ Personalización visual (colores, tipografía)
- ✅ Autoguardado automático

## 📋 Requisitos

- Navegador moderno (Chrome, Firefox, Safari, Edge)
- Cuenta de Google (opcional, para sincronización en la nube)
- Proyecto de Firebase (para backend)

## 🔧 Configuración de Firebase

### Paso 1: Crear proyecto en Firebase

1. Ve a [Firebase Console](https://console.firebase.google.com/)
2. Haz clic en **"Agregar proyecto"**
3. Nombra tu proyecto (ej: `agenda-docente`)
4. Sigue el asistente (puedes desactivar Google Analytics si quieres)

### Paso 2: Obtener credenciales

1. En tu proyecto, haz clic en el ícono **⚙️ web** (`</>`) para agregar una app web
2. Registra la app con un nombre (ej: `Agenda Docente Web`)
3. Copia el objeto `firebaseConfig` que te da Firebase

### Paso 3: Configurar Authentication

1. En el menú lateral de Firebase, ve a **Authentication**
2. Haz clic en **"Comenzar"**
3. En la pestaña **Sign-in method**, activa **Google**
4. Configura un email de soporte público

### Paso 4: Configurar Firestore

1. En el menú lateral, ve a **Firestore Database**
2. Haz clic en **"Crear base de datos"**
3. Elige **"Comenzar en modo de prueba"** (luego cambiaremos a producción)
4. Selecciona la ubicación más cercana a ti

### Paso 5: Pegar credenciales en el código

Abre `index.html` y busca esta sección:

```javascript
const firebaseConfig = {
  apiKey: "TU_API_KEY_AQUI",
  authDomain: "TU_PROYECTO.firebaseapp.com",
  projectId: "TU_PROJECT_ID",
  storageBucket: "TU_PROYECTO.appspot.com",
  messagingSenderId: "TU_SENDER_ID",
  appId: "TU_APP_ID"
};
```

Reemplaza los valores con los de tu proyecto.

### Paso 6: Aplicar reglas de seguridad

1. En Firebase, ve a **Firestore Database → Reglas**
2. Copia y pega el contenido de `firestore.rules`
3. Haz clic en **Publicar**

## 🌐 Despliegue en GitHub Pages

### Opción A: Despliegue directo

1. Sube `index.html` a un repositorio de GitHub
2. Ve a **Settings → Pages**
3. Selecciona la rama `main` y carpeta `/root`
4. Tu app estará en `https://tu-usuario.github.io/tu-repo/`

### Opción B: Firebase Hosting (recomendado)

```bash
# Instalar Firebase CLI
npm install -g firebase-tools

# Login
firebase login

# Inicializar hosting
firebase init hosting

# Seleccionar proyecto y carpeta pública (./)
# Configurar como SPA: Yes

# Desplegar
firebase deploy
```

## 📁 Estructura del proyecto

```
agenda-docente/
├── index.html          # Aplicación completa (HTML + CSS + JS)
├── firestore.rules     # Reglas de seguridad de Firestore
└── README.md           # Esta guía
```

## 🎯 Fases de desarrollo

- **Fase 1** ✅ Estructura base, auth, navegación, guardado
- **Fase 2** 🔄 Instituciones, materias, horarios, calendarios
- **Fase 3** 📋 Alumnado, evaluación, rúbricas
- **Fase 4** 📚 Planeación, bienestar, exportación PDF
- **Fase 5** 🔗 Integración con Google Calendar

## 🔒 Seguridad

- Cada usuario solo accede a sus propios datos
- Reglas de Firestore validan la propiedad de los documentos
- Autenticación obligatoria para acceder a datos en la nube
- Modo local disponible para uso sin cuenta

## 🛠️ Tecnologías

- HTML5, CSS3, JavaScript vanilla
- Firebase (Auth + Firestore)
- Lucide Icons
- Google Fonts (Inter, Montserrat)

## 📝 Licencia

Uso educativo y profesional. Modifica y adapta según tus necesidades.

## 🤝 Soporte

Para reportar problemas o sugerir mejoras, abre un issue en el repositorio.

---

**Hecho con ❤️ para docentes que quieren organizar su año con claridad y motivación.**
