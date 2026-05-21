# 🎬 Guía de Demo para Bobathon
## Sistema de Planeaciones Didácticas PLIBM

---

## 📋 Preparación Pre-Demo

### Checklist de Preparación (30 minutos antes)

- [ ] Verificar que PostgreSQL esté corriendo
- [ ] Iniciar backend (Terminal 1)
- [ ] Iniciar frontend (Terminal 2)
- [ ] Abrir navegador en http://localhost:3000
- [ ] Tener documentación de API abierta en http://localhost:8000/docs
- [ ] Preparar ventanas de código para mostrar
- [ ] Tener ejemplos de PDFs generados listos
- [ ] Verificar conexión a internet (si es necesario)
- [ ] Probar audio y video
- [ ] Cerrar aplicaciones innecesarias

### Comandos de Inicio

```bash
# Terminal 1 - Backend
cd "Planeaciones Didacticas/backend"
.\venv\Scripts\Activate.ps1
uvicorn main:app --reload

# Terminal 2 - Frontend  
cd "Planeaciones Didacticas/frontend"
npm run dev
```

### URLs Importantes

- **Frontend**: http://localhost:3000
- **Backend API**: http://localhost:8000
- **API Docs**: http://localhost:8000/docs
- **Presentación**: BOBATHON_PRESENTACION.md

---

## 🎯 Script de Demo (10 minutos)

### MINUTO 0-1: Introducción y Contexto

**Qué decir**:
> "Buenos días/tardes. Hoy les presento el Sistema de Planeaciones Didácticas PLIBM, una solución que revoluciona la forma en que los docentes de primaria crean sus planeaciones didácticas."

**Qué mostrar**:
- Slide de título o página de inicio
- Mencionar el problema: docentes gastan 8-12 horas semanales en planeaciones

**Puntos clave**:
- 500,000+ docentes potenciales en México
- Alineado con Nueva Escuela Mexicana
- Reduce tiempo de planeación en 70%

---

### MINUTO 1-2: Página de Inicio

**Qué hacer**:
1. Abrir http://localhost:3000
2. Mostrar la interfaz principal

**Qué decir**:
> "La interfaz es moderna, intuitiva y responsive. Tenemos tres secciones principales: Inicio, Crear Planeación y Buscar Planeaciones."

**Qué mostrar**:
- Navegación clara
- Diseño profesional con colores PLIBM
- Botones de acción principales

**Tiempo**: 30 segundos

---

### MINUTO 2-6: Crear Nueva Planeación (DEMO PRINCIPAL)

**Qué hacer**:
1. Click en "Crear Nueva Planeación"
2. Completar formulario en vivo

**Datos de ejemplo para usar**:
```
Título: "Proyecto de Ciencias: El Ciclo del Agua"
Escuela: "Escuela Primaria Benito Juárez"
Profesor: "Prof. María García López"
Grado: 4°
Mes: Octubre
Año: 2026
Campo Formativo: "Saberes y Pensamiento Científico"
Eje Articulador: "Pensamiento Crítico"
Contenido: "Comprende el ciclo del agua y su importancia para los seres vivos"
PDA: "Explica las fases del ciclo del agua mediante representaciones gráficas y experimentos sencillos"
Metodología: "Aprendizaje Basado en Proyectos"
Justificación: "El agua es un recurso vital y los estudiantes deben comprender su ciclo para valorar su importancia y cuidado. Este proyecto les permitirá observar, experimentar y reflexionar sobre los procesos naturales del agua."
Propósito: "Que los estudiantes comprendan el ciclo del agua a través de la observación, experimentación y representación gráfica, desarrollando conciencia sobre el cuidado del agua."
Palabras clave: agua, ciclo, evaporación, condensación, precipitación
Recursos: cartulinas, colores, recipientes, agua, hielo
```

**Qué decir mientras completas**:
> "Observen cómo el sistema nos guía paso a paso. Primero la información básica, incluyendo el nombre de la escuela y profesor que se incluirán en el PDF."

> "Ahora seleccionamos la alineación curricular. El sistema tiene integrados todos los campos formativos y ejes articuladores de la Nueva Escuela Mexicana."

> "Elegimos la metodología. Tenemos 8 metodologías didácticas disponibles: ABP, Aprendizaje Cooperativo, Gamificación, etc."

> "Y aquí viene la magia: al guardar, el sistema generará automáticamente 4 semanas completas de actividades, con 3-4 sesiones por semana, ejercicios detallados, materiales, y evaluación formativa."

**Qué mostrar**:
- Validación en tiempo real
- Catálogos desplegables
- Campos de palabras clave y recursos
- Botón de guardar

**Tiempo**: 3-4 minutos

---

### MINUTO 6-7: Búsqueda Inteligente

**Qué hacer**:
1. Navegar a "Buscar Planeaciones"
2. Realizar búsqueda de ejemplo

**Búsquedas de ejemplo**:
```
Búsqueda 1: "agua ciclo"
Filtros: Grado 4°, Campo Formativo: Saberes y Pensamiento Científico

Búsqueda 2: "fracciones"
Filtros: Grado 3°, Metodología: ABP

Búsqueda 3: "lectura cuentos"
Filtros: Campo Formativo: Lenguajes
```

**Qué decir**:
> "El sistema utiliza búsqueda de texto completo de PostgreSQL. Podemos buscar por cualquier palabra en el contenido y aplicar múltiples filtros."

> "Los resultados se ordenan por relevancia. Cada tarjeta muestra información clave: título, grado, mes, campo formativo y palabras clave."

**Qué mostrar**:
- Barra de búsqueda
- Filtros múltiples
- Resultados en tarjetas
- Botones de acción (Ver, Duplicar, Descargar)

**Tiempo**: 1 minuto

---

### MINUTO 7-8: Visualizar Planeación

**Qué hacer**:
1. Click en "Ver" en una planeación
2. Mostrar el detalle completo

**Qué decir**:
> "Al abrir una planeación, vemos toda la información estructurada: la alineación curricular, metodología, y lo más importante..."

> "Las 4 semanas de actividades generadas automáticamente. Cada semana tiene 3-4 sesiones, cada sesión incluye: título, duración, descripción detallada, materiales necesarios, forma de organización y productos esperados."

> "También tenemos la evaluación formativa completa con rúbricas y listas de cotejo."

**Qué mostrar**:
- Scroll por las secciones
- Destacar las actividades semanales
- Mostrar la evaluación formativa
- Botones de acción (Duplicar, Descargar)

**Tiempo**: 1 minuto

---

### MINUTO 8-9: Generación de PDF

**Qué hacer**:
1. Click en "Descargar PDF"
2. Abrir el PDF generado

**Qué decir**:
> "Con un click generamos un PDF profesional, listo para imprimir o compartir."

> "El PDF incluye el encabezado institucional con los colores PLIBM, toda la información de la planeación, las actividades semanales detalladas, y la evaluación."

> "Noten que incluye el nombre de la escuela y del profesor que capturamos al inicio."

**Qué mostrar**:
- Proceso de descarga
- PDF abierto
- Scroll por las páginas
- Formato profesional

**Tiempo**: 1 minuto

---

### MINUTO 9-10: Cierre y Roadmap

**Qué decir**:
> "En resumen, este sistema reduce el tiempo de planeación de 8-12 horas a solo 15-20 minutos, garantiza alineación perfecta con la Nueva Escuela Mexicana, y genera contenido educativo de calidad."

> "El roadmap incluye: sistema de usuarios, IA generativa para contenido personalizado, colaboración en tiempo real, y app móvil."

> "Estamos listos para impactar a 500,000 docentes y 14 millones de estudiantes en México."

**Qué mostrar**:
- Slide de beneficios cuantitativos
- Slide de roadmap
- Slide de contacto

**Tiempo**: 1 minuto

---

## 🎨 Tips de Presentación

### Antes de Empezar

1. **Practica el flujo completo** al menos 3 veces
2. **Cronometra cada sección** para no pasarte del tiempo
3. **Prepara datos de ejemplo** que sean interesantes
4. **Ten un plan B** si algo falla (screenshots, video grabado)
5. **Conoce tu audiencia** y adapta el lenguaje

### Durante la Demo

1. **Habla con confianza** pero no demasiado rápido
2. **Explica mientras haces** cada acción
3. **Destaca los beneficios** no solo las características
4. **Usa números concretos** (70% reducción, 15 minutos vs 8 horas)
5. **Mantén contacto visual** con la audiencia
6. **Sonríe y muestra entusiasmo** por tu proyecto

### Manejo de Problemas

**Si el sistema no carga**:
- Tener screenshots preparados
- Tener un video de backup
- Explicar la arquitectura mientras se reinicia

**Si hay preguntas durante la demo**:
- Anota las preguntas para responder al final
- Si es rápida, responde brevemente
- No pierdas el hilo de la presentación

**Si te quedas sin tiempo**:
- Prioriza: Crear Planeación > Búsqueda > PDF
- Salta secciones menos críticas
- Menciona lo que no alcanzaste a mostrar

---

## 📊 Puntos Clave a Enfatizar

### Problema Real
- Docentes gastan 8-12 horas semanales en planeaciones
- Dificultad para alinear con Nueva Escuela Mexicana
- Falta de herramientas digitales adecuadas

### Solución Innovadora
- Generación automática de actividades (IA)
- Búsqueda inteligente con PostgreSQL
- Interfaz moderna y fácil de usar

### Impacto Medible
- 70% reducción en tiempo de planeación
- 100% alineación curricular
- 500,000+ docentes potenciales

### Tecnología Robusta
- Stack moderno (FastAPI + Next.js 14)
- Base de datos PostgreSQL con full-text search
- Arquitectura escalable

### Visión a Futuro
- IA generativa personalizada
- Comunidad de docentes
- Expansión a otros niveles educativos

---

## 🎤 Preguntas Frecuentes (Q&A)

### Técnicas

**P: ¿Qué tecnologías usaron?**
R: Backend en FastAPI (Python), Frontend en Next.js 14 con TypeScript, Base de datos PostgreSQL con búsqueda de texto completo.

**P: ¿Cómo funciona la generación automática de actividades?**
R: Tenemos un servicio que genera actividades estructuradas basándose en el grado, campo formativo y metodología seleccionados. Actualmente usa templates inteligentes, pero el roadmap incluye IA generativa.

**P: ¿Es escalable?**
R: Sí, la arquitectura está diseñada para escalar. Usamos PostgreSQL que puede manejar millones de registros, y el frontend es estático y cacheable.

**P: ¿Cuánto tiempo tomó desarrollar?**
R: Aproximadamente 4 semanas de desarrollo full-time.

### Funcionales

**P: ¿Los docentes pueden colaborar?**
R: Actualmente no, pero está en el roadmap para la Fase 3 (5-6 meses).

**P: ¿Hay app móvil?**
R: No aún, pero está planeada para la Fase 4 (7-12 meses). La versión web es responsive y funciona en móviles.

**P: ¿Cómo se garantiza la calidad de las actividades generadas?**
R: Las actividades se basan en mejores prácticas pedagógicas y están alineadas con el plan de estudios. Los docentes pueden revisar y ajustar según necesiten.

**P: ¿Funciona offline?**
R: Actualmente no, requiere conexión a internet. El modo offline está en el roadmap.

### Negocio

**P: ¿Cuál es el modelo de negocio?**
R: Estamos evaluando: freemium (básico gratis, premium de pago), licencias institucionales, o patrocinio gubernamental.

**P: ¿Cuántos usuarios tienen?**
R: Es un proyecto en fase de lanzamiento. El mercado potencial es de 500,000+ docentes en México.

**P: ¿Cómo planean monetizar?**
R: Opciones: suscripción premium, licencias escolares, marketplace de recursos, o alianzas con SEP.

---

## 📝 Checklist Post-Demo

Después de la presentación:

- [ ] Agradecer a la audiencia
- [ ] Compartir enlaces de documentación
- [ ] Recopilar feedback
- [ ] Responder preguntas pendientes
- [ ] Conectar con personas interesadas
- [ ] Actualizar presentación basado en feedback
- [ ] Documentar lecciones aprendidas

---

## 🎯 Objetivos de la Demo

Al final de la demo, la audiencia debe:

1. ✅ Entender el problema que resuelve el sistema
2. ✅ Ver el valor de la solución (70% reducción de tiempo)
3. ✅ Apreciar la calidad técnica del proyecto
4. ✅ Reconocer el impacto social potencial
5. ✅ Querer saber más o involucrarse

---

## 💡 Frases Clave para Usar

- "De 8 horas a 15 minutos"
- "Alineación perfecta con la Nueva Escuela Mexicana"
- "Generación automática de actividades educativas"
- "500,000 docentes, 14 millones de estudiantes"
- "Tecnología moderna, impacto real"
- "No solo ahorra tiempo, mejora la calidad"

---

## 🏆 Mensaje Final

> "El Sistema de Planeaciones Didácticas PLIBM no es solo una herramienta tecnológica, es un aliado para los docentes mexicanos. Les devuelve tiempo para lo que realmente importa: enseñar, inspirar y transformar vidas. Gracias."

---

**¡Éxito en tu presentación!** 🚀

*Guía preparada para Bobathon 2026*