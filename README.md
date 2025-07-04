# BAQ Home - Proyecto Full Stack

Este repositorio contiene dos proyectos principales que conforman la aplicación BAQ Home: un frontend en React/TypeScript y un backend en NestJS.

## Repositorios del Proyecto

- Frontend: [baq-home](https://github.com/ejcondorf88/baq-home)
- Backend: [baq-home-backend](https://github.com/ejcondorf88/baq-home-backend)

## Estructura del Repositorio

### Importante: Configuración de Git
Este proyecto utiliza una estructura monorepo. Para evitar problemas con repositorios Git anidados, sigue estos pasos:

1. Elimina los repositorios Git anidados:
```bash
# Eliminar el repositorio Git del backend
git rm --cached baq-home-backend
rm -rf baq-home-backend/.git

# Eliminar el repositorio Git del frontend
git rm --cached baq-home
rm -rf baq-home/.git
```

2. Asegúrate de que solo existe un repositorio Git en la raíz del proyecto:
```bash
# Verificar que solo existe un .git en la raíz
ls -la .git
```


### Estructura de Carpetas
```
.
├── baq-home/           # Frontend (React + TypeScript + Vite)
└── baq-home-backend/   # Backend (NestJS + TypeScript)
```

## Pasos para Correr el Proyecto

1. **Clonar el Repositorio Principal**:
   ```bash
   git clone https://github.com/ejcondorf88/general-baq.gitls
   ```

2. **Clonar los Sub-repositorios**:
   - Clonar el repositorio de frontend:
     ```bash
     git clone https://github.com/ejcondorf88/baq-home.git baq-home
     ```
   - Clonar el repositorio de backend:
     ```bash
     git clone https://github.com/ejcondorf88/baq-home-backend.git baq-home-backend
     ```

3. **Instalar Dependencias**:
   - Para el frontend:
     ```bash
     cd baq-home
     npm install
     ```
   - Para el backend:
     ```bash
     cd baq-home-backend
     npm install
     ```

4. **Configurar Variables de Entorno**:
   - Frontend: Crea un archivo `.env` en la carpeta `baq-home` con el siguiente contenido:
     ```env
     VITE_API_URL=http://localhost:3000
     ```
   - Backend: Crea un archivo `.env` en la carpeta `baq-home-backend` con el siguiente contenido:
     ```env
     DATABASE_URL=postgresql://user:password@localhost:5432/baq_home
     JWT_SECRET=your-secret-key
     ```

5. **Iniciar el Desarrollo**:
   - Frontend:
     ```bash
     cd baq-home
     npm run dev
     ```
   - Backend:
     ```bash
     cd baq-home-backend
     npm run start:dev
     ```

## Frontend (baq-home)

El frontend es una aplicación web moderna construida con:
- React
- TypeScript
- Vite
- Tailwind CSS

### Requisitos
- Node.js (versión recomendada: 18.x o superior)
- npm o yarn

### Instalación
```bash
cd baq-home
npm install
```

### Desarrollo
```bash
npm run dev
```

### Construcción
```bash
npm run build
```

## Backend (baq-home-backend)

El backend es una API REST construida con:
- NestJS
- TypeScript
- TypeORM
- PostgreSQL

### Requisitos
- Node.js (versión recomendada: 18.x o superior)
- npm o yarn
- PostgreSQL

### Instalación
```bash
cd baq-home-backend
npm install
```

### Desarrollo
```bash
npm run start:dev
```

### Construcción
```bash
npm run build
```

## Variables de Entorno

### Frontend (.env)
```env
VITE_API_URL=http://localhost:3000
```

### Backend (.env)
```env
DATABASE_URL=postgresql://user:password@localhost:5432/baq_home
JWT_SECRET=your-secret-key
```

## Scripts Disponibles

### Frontend
- `npm run dev`: Inicia el servidor de desarrollo
- `npm run build`: Construye la aplicación para producción
- `npm run preview`: Vista previa de la versión de producción
- `npm run lint`: Ejecuta el linter
- `npm run test`: Ejecuta las pruebas

### Backend
- `npm run start`: Inicia la aplicación
- `npm run start:dev`: Inicia la aplicación en modo desarrollo
- `npm run build`: Compila la aplicación
- `npm run test`: Ejecuta las pruebas unitarias
- `npm run test:e2e`: Ejecuta las pruebas end-to-end

## Contribución

1. Fork el repositorio
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## Contribuidores

### Desarrolladores Principales
- Salome Polanco - Desarrolladora Frontend
- Erik Olalla - Desarrollador Backend
- Elian Condor - Desarrollador Full Stack

### Roles y Responsabilidades
- **Frontend**: Desarrollo de interfaces de usuario, implementación de componentes React, integración con APIs
- **Backend**: Diseño de APIs REST, implementación de servicios, gestión de base de datos
- **Full Stack**: Coordinación de desarrollo, integración frontend-backend, optimización de rendimiento

### Tecnologías Principales
- React + TypeScript
- NestJS
- PostgreSQL
- Tailwind CSS
- TypeORM

### Estadísticas del Proyecto
- Frontend: 94.2% TypeScript, 2.8% JavaScript, 1.9% CSS, 1.1% HTML
- Backend: 98.1% TypeScript, 1.9% JavaScript

## Licencia

Este proyecto está bajo la Licencia MIT - ver el archivo [LICENSE](LICENSE) para más detalles.

## Nota Importante
Al clonar el repositorio principal, las carpetas de los sub-repositorios (`baq-home` y `baq-home-backend`) se generarán vacías. Para obtener el contenido completo de estos sub-repositorios, debes clonarlos por separado.
