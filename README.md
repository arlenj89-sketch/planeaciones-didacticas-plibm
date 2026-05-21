# planeaciones-didacticas-plibm
Sistema de Planeaciones Didácticas alineado con la Nueva Escuela Mexicana
- **Nombre**: Arlen Dinora Jimenez Elizondo / Reyna Velazquez
- **GitHub**: https://github.com/arlenj89-sketch
- **Email**: ad.jimenez@ibm.com
# Sistema de Planeaciones Didácticas PLIBM

Aplicación web para automatizar la creación de planeaciones didácticas mensuales alineadas con la Nueva Escuela Mexicana.

## 🎯 Características Principales

- ✅ Alineación con Planes y Programas PLIBM vigentes
- 📝 Generador inteligente de planeaciones mensuales
- 🔍 Búsqueda avanzada con filtros múltiples
- 🤖 Sugerencias de IA para evaluaciones
- 📄 Exportación a PDF
- 🔄 Duplicación y edición de planeaciones

## 🏗️ Arquitectura del Sistema

### Stack Tecnológico

**Frontend:**
- Next.js 14+ (App Router) con TypeScript
- Tailwind CSS + shadcn/ui
- React Hook Form + Zod
- TanStack Query
- jsPDF para exportación PDF

**Backend:**
- FastAPI (Python 3.11+)
- Pydantic para validación
- OpenAI API para sugerencias IA
- SQLAlchemy ORM

**Base de Datos:**
- PostgreSQL 15+ con full-text search
- Índices optimizados para búsqueda

### Justificación Técnica

1. **Next.js**: SSR/SSG para mejor rendimiento y SEO, ideal para aplicaciones educativas
2. **FastAPI**: Alto rendimiento, async nativo, excelente para integración con IA
3. **PostgreSQL**: Búsqueda full-text avanzada, relaciones complejas, escalabilidad
4. **TypeScript**: Type-safety end-to-end, reduce errores en producción

## 📊 Modelo de Datos

Ver [`docs/DATABASE_SCHEMA.md`](docs/DATABASE_SCHEMA.md) para el esquema completo.

## 🚀 Inicio Rápido

### Prerrequisitos

- Node.js 18+
- Python 3.11+
- PostgreSQL 15+
- OpenAI API Key (opcional, para sugerencias IA)

### Instalación

```bash
# Clonar repositorio
git clone <repo-url>
cd planeaciones-sep

# Instalar dependencias frontend
cd frontend
npm install

# Instalar dependencias backend
cd ../backend
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt

# Configurar base de datos
createdb planeaciones_sep
cd backend
alembic upgrade head
```

### Configuración

Crear archivo `.env` en `/backend`:

```env
DATABASE_URL=postgresql://user:password@localhost:5432/planeaciones_sep
OPENAI_API_KEY=sk-...
SECRET_KEY=your-secret-key-here
```

Crear archivo `.env.local` en `/frontend`:

```env
NEXT_PUBLIC_API_URL=http://localhost:8000
```

### Ejecutar

```bash
# Terminal 1 - Backend
cd backend
uvicorn main:app --reload

# Terminal 2 - Frontend
cd frontend
npm run dev
```

Acceder a: http://localhost:3000

## 📁 Estructura del Proyecto

```
planeaciones-sep/
├── frontend/                 # Next.js application
│   ├── app/                 # App router pages
│   ├── components/          # React components
│   ├── lib/                 # Utilities
│   └── types/               # TypeScript types
├── backend/                 # FastAPI application
│   ├── api/                 # API routes
│   ├── models/              # Database models
│   ├── schemas/             # Pydantic schemas
│   ├── services/            # Business logic
│   └── main.py              # App entry point
└── docs/                    # Documentation
```

## 📖 Documentación

- [Esquema de Base de Datos](docs/DATABASE_SCHEMA.md)
- [API Reference](docs/API_REFERENCE.md)
- [Guía de Uso](docs/USER_GUIDE.md)

## 🤝 Contribuir

Ver [CONTRIBUTING.md](CONTRIBUTING.md) para guías de contribución.

## 📄 Licencia

MIT License - Ver [LICENSE](LICENSE) para más detalles.
