# 🔀 Guía para Fork del Repositorio - Bobathon
## Sistema de Planeaciones Didácticas PLIBM

---

## 📋 ¿Qué es un Fork?

Un **Fork** es una copia de un repositorio de GitHub que se crea en tu propia cuenta. Te permite:
- Tener tu propia versión del proyecto
- Hacer cambios sin afectar el original
- Contribuir de vuelta al proyecto original (Pull Request)
- Participar en el Bobathon con tu versión

---

## 🎯 Paso 1: Preparar tu Cuenta de GitHub

### Si NO tienes cuenta de GitHub:

1. **Ve a** [github.com](https://github.com)
2. **Click en "Sign up"** (Registrarse)
3. **Completa el formulario**:
   - Email
   - Contraseña
   - Nombre de usuario
4. **Verifica tu email**
5. **Completa tu perfil** (opcional pero recomendado)

### Si YA tienes cuenta:

1. **Inicia sesión** en [github.com](https://github.com)
2. **Verifica que estés logueado** (tu foto de perfil aparece arriba a la derecha)

---

## 🔀 Paso 2: Hacer Fork del Repositorio

### Opción A: Si el repositorio ya está en GitHub

1. **Abre el repositorio original** en GitHub
   - URL ejemplo: `https://github.com/usuario-original/planeaciones-didacticas`

2. **Busca el botón "Fork"** en la esquina superior derecha
   ```
   ┌─────────────────────────────────────┐
   │  ⭐ Star    👁 Watch    🔀 Fork     │
   └─────────────────────────────────────┘
   ```

3. **Click en "Fork"**

4. **Selecciona tu cuenta** como destino del fork
   - Si perteneces a organizaciones, elige dónde crear el fork

5. **Espera a que se complete** el proceso (10-30 segundos)

6. **¡Listo!** Ahora tienes tu propia copia en:
   `https://github.com/TU-USUARIO/planeaciones-didacticas`

### Opción B: Si el proyecto está solo en tu computadora

Si el proyecto aún no está en GitHub, necesitas subirlo primero:

#### 1. Crear un nuevo repositorio en GitHub

1. **Ve a** [github.com/new](https://github.com/new)
2. **Completa la información**:
   - Repository name: `planeaciones-didacticas-plibm`
   - Description: `Sistema de Planeaciones Didácticas alineado con la Nueva Escuela Mexicana`
   - Visibility: `Public` (para Bobathon)
   - ❌ NO inicialices con README (ya tienes uno)
3. **Click en "Create repository"**

#### 2. Subir tu proyecto local a GitHub

Abre una terminal en la carpeta del proyecto y ejecuta:

```bash
# Navegar a la carpeta del proyecto
cd "c:/Users/ArlenDinoraJimenezEl/Desktop/BOB/Planeaciones Didacticas"

# Inicializar Git (si no está inicializado)
git init

# Agregar todos los archivos
git add .

# Hacer el primer commit
git commit -m "Initial commit: Sistema de Planeaciones Didácticas PLIBM"

# Conectar con GitHub (reemplaza TU-USUARIO con tu usuario de GitHub)
git remote add origin https://github.com/TU-USUARIO/planeaciones-didacticas-plibm.git

# Subir el código
git branch -M main
git push -u origin main
```

**Nota**: GitHub te pedirá autenticación. Usa tu usuario y contraseña, o mejor aún, un Personal Access Token.

---

## 📥 Paso 3: Clonar tu Fork a tu Computadora

Si quieres trabajar en tu fork desde tu computadora:

```bash
# Clonar tu fork
git clone https://github.com/TU-USUARIO/planeaciones-didacticas-plibm.git

# Entrar a la carpeta
cd planeaciones-didacticas-plibm

# Verificar que está conectado a tu fork
git remote -v
```

---

## 🔄 Paso 4: Mantener tu Fork Actualizado

Si el repositorio original recibe actualizaciones, puedes sincronizar tu fork:

### Desde GitHub (Interfaz Web):

1. **Ve a tu fork** en GitHub
2. **Busca el mensaje** "This branch is X commits behind..."
3. **Click en "Sync fork"**
4. **Click en "Update branch"**

### Desde la Terminal:

```bash
# Agregar el repositorio original como "upstream"
git remote add upstream https://github.com/usuario-original/planeaciones-didacticas.git

# Obtener los cambios del original
git fetch upstream

# Fusionar los cambios en tu rama main
git checkout main
git merge upstream/main

# Subir los cambios a tu fork
git push origin main
```

---

## 📝 Paso 5: Preparar para el Bobathon

### 1. Actualizar el README

Edita el archivo `README.md` para incluir:

```markdown
# 🎓 Sistema de Planeaciones Didácticas PLIBM

> Proyecto para Bobathon 2026

## 👤 Autor
- **Nombre**: [Tu Nombre]
- **GitHub**: [@tu-usuario](https://github.com/tu-usuario)
- **Email**: tu-email@ejemplo.com

## 🏆 Bobathon
Este proyecto participa en el Bobathon 2026 en la categoría de Educación.

[... resto del README ...]
```

### 2. Agregar Licencia

Crea un archivo `LICENSE` con la licencia que prefieras:
- MIT (recomendada para proyectos open source)
- Apache 2.0
- GPL v3

### 3. Agregar .gitignore

Asegúrate de tener un `.gitignore` para no subir archivos innecesarios:

```gitignore
# Python
__pycache__/
*.py[cod]
*$py.class
*.so
.Python
venv/
env/
*.egg-info/

# Node
node_modules/
.next/
out/
build/
dist/

# Environment
.env
.env.local

# IDE
.vscode/
.idea/
*.swp
*.swo

# OS
.DS_Store
Thumbs.db

# Database
*.db
*.sqlite
```

### 4. Crear un Release

Para el Bobathon, crea un release:

1. **Ve a tu repositorio** en GitHub
2. **Click en "Releases"** (lado derecho)
3. **Click en "Create a new release"**
4. **Completa**:
   - Tag: `v1.0.0-bobathon`
   - Title: `Bobathon 2026 - Sistema de Planeaciones Didácticas`
   - Description: Resumen del proyecto y características
5. **Click en "Publish release"**

---

## 🎬 Paso 6: Preparar la Presentación

### 1. Agregar Screenshots

Crea una carpeta `screenshots/` y agrega imágenes:

```
screenshots/
├── home.png
├── crear-planeacion.png
├── buscar.png
├── pdf-generado.png
└── arquitectura.png
```

### 2. Crear un Video Demo

Graba un video de 2-3 minutos mostrando:
- Página de inicio
- Crear una planeación
- Buscar planeaciones
- Descargar PDF

Súbelo a YouTube y agrega el link al README.

### 3. Documentación Completa

Asegúrate de tener todos estos archivos:
- ✅ `README.md` - Descripción general
- ✅ `BOBATHON_PRESENTACION.md` - Presentación completa
- ✅ `BOBATHON_GUIA_DEMO.md` - Guía de demo
- ✅ `BOBATHON_CASOS_DE_USO.md` - Casos de uso
- ✅ `GUIA_COMPLETA_INSTALACION.md` - Instalación
- ✅ `ARQUITECTURA_Y_JUSTIFICACION.md` - Arquitectura

---

## 🚀 Paso 7: Registrar en el Bobathon

1. **Ve al sitio del Bobathon**
2. **Completa el formulario de registro**:
   - Nombre del proyecto
   - URL del repositorio de GitHub
   - Categoría: Educación
   - Descripción breve
   - Video demo (si lo tienes)
3. **Envía tu registro**

---

## 📊 Checklist Final

Antes de presentar, verifica:

### Repositorio
- [ ] Fork creado en tu cuenta de GitHub
- [ ] Código subido y actualizado
- [ ] README.md completo con información del Bobathon
- [ ] LICENSE agregada
- [ ] .gitignore configurado
- [ ] Release v1.0.0-bobathon creado

### Documentación
- [ ] BOBATHON_PRESENTACION.md
- [ ] BOBATHON_GUIA_DEMO.md
- [ ] BOBATHON_CASOS_DE_USO.md
- [ ] GUIA_COMPLETA_INSTALACION.md
- [ ] ARQUITECTURA_Y_JUSTIFICACION.md

### Multimedia
- [ ] Screenshots en carpeta screenshots/
- [ ] Video demo grabado y subido
- [ ] Link del video en README

### Sistema
- [ ] Backend funciona correctamente
- [ ] Frontend funciona correctamente
- [ ] Base de datos configurada
- [ ] Datos de prueba cargados
- [ ] PDFs se generan correctamente

### Presentación
- [ ] Slides preparadas
- [ ] Demo practicada 3 veces
- [ ] Datos de ejemplo listos
- [ ] Plan B preparado (screenshots/video)

---

## 💡 Tips Importantes

### Para el Fork

1. **Nombre descriptivo**: Usa un nombre claro para tu repositorio
2. **Descripción completa**: Explica qué hace el proyecto
3. **Topics/Tags**: Agrega tags relevantes (education, mexico, fastapi, nextjs)
4. **README atractivo**: Primera impresión cuenta
5. **Commits claros**: Mensajes de commit descriptivos

### Para el Bobathon

1. **Destaca el impacto**: 500,000 docentes, 14 millones de estudiantes
2. **Muestra números**: 70% reducción de tiempo
3. **Cuenta historias**: Usa los casos de uso
4. **Demo fluida**: Practica hasta que sea natural
5. **Sé auténtico**: Muestra tu pasión por la educación

---

## 🆘 Solución de Problemas

### "No puedo hacer fork"
- Verifica que estés logueado en GitHub
- Asegúrate de tener permisos
- Intenta desde otro navegador

### "Git no está instalado"
```bash
# Descargar Git desde:
https://git-scm.com/download/win
```

### "Error al hacer push"
- Verifica tu autenticación
- Usa Personal Access Token en lugar de contraseña
- Revisa que la URL del remote sea correcta

### "El repositorio es muy grande"
- Revisa el .gitignore
- No subas node_modules/ ni venv/
- No subas archivos de base de datos

---

## 📞 Recursos Adicionales

### GitHub
- [GitHub Docs - Fork](https://docs.github.com/en/get-started/quickstart/fork-a-repo)
- [GitHub Guides](https://guides.github.com/)

### Git
- [Git Handbook](https://guides.github.com/introduction/git-handbook/)
- [Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)

### Bobathon
- Sitio oficial del Bobathon
- Reglas y categorías
- Fechas importantes

---

## ✅ Resumen Rápido

```bash
# 1. Hacer fork en GitHub (botón Fork)

# 2. Clonar tu fork
git clone https://github.com/TU-USUARIO/planeaciones-didacticas-plibm.git

# 3. Hacer cambios
cd planeaciones-didacticas-plibm
# ... editar archivos ...

# 4. Guardar cambios
git add .
git commit -m "Preparación para Bobathon"
git push origin main

# 5. Crear release en GitHub

# 6. Registrar en Bobathon
```

---

## 🏆 ¡Éxito en el Bobathon!

Tienes un proyecto excelente con:
- ✅ Código funcional y bien estructurado
- ✅ Documentación completa
- ✅ Impacto social real
- ✅ Tecnología moderna

**¡Estás listo para brillar!** 🌟

---

*Guía preparada para Bobathon 2026*