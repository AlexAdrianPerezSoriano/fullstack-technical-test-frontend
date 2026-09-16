# 🎟️ Ticket Reservation System - Frontend

## 📌 Descripción
Interfaz de usuario para el sistema de reserva de tickets. Permite ver eventos, reservar tickets y gestionar eventos (solo admin). Desarrollado con React, Vite y TailwindCSS.

## 🚀 Tecnologías
- React (v18)
- Vite (v8)
- TailwindCSS (v4)
- Axios (Consumo de API)
- React Router (Navegación)
- Docker (Contenerización)

## 📁 Estructura del Proyecto

frontend/
├── src/
│   ├── api/
│   │   └── axiosConfig.js     # Configuración de Axios
│   ├── components/
│   │   ├── EventList.jsx
│   │   ├── EventDetail.jsx
│   │   ├── ReservationForm.jsx
│   │   ├── ReservationConfirmation.jsx
│   │   └── ProtectedRoute.jsx
│   ├── context/
│   │   └── AuthContext.jsx    # Contexto de autenticación
│   ├── pages/
│   │   ├── Home.jsx
│   │   ├── Login.jsx
│   │   ├── Register.jsx
│   │   └── EventPage.jsx
│   ├── App.jsx
│   └── main.jsx
├── public/
├── Dockerfile
├── docker-compose.yml
├── package.json
├── .env.example
└── .gitignore

## 📦 Instalación y Ejecución

### Opción 1: Con Docker (Recomendado)
git clone https://github.com/AlexAdrianPerezSoriano/ticket-frontend.git
cd ticket-frontend
docker compose up --build

La aplicación estará disponible en: http://localhost

### Opción 2: Desarrollo local
npm install
cp .env.example .env  # Configura la URL del backend
npm run dev           # Inicia el servidor

## 🔧 Variables de Entorno (.env)
Crea un archivo .env basado en .env.example:

VITE_API_URL=http://localhost:5000

En producción: Cambia VITE_API_URL por la URL del backend desplegado.

## 👥 Roles y Permisos

| Acción | Usuario Estándar | Administrador |
|--------|------------------|---------------|
| Ver eventos | ✅ | ✅ |
| Ver detalles | ✅ | ✅ |
| Reservar tickets | ✅ | ✅ |
| Crear eventos | ❌ | ✅ |
| Editar eventos | ❌ | ✅ |
| Eliminar eventos | ❌ | ✅ |

## 👥 Credenciales de Prueba
- Admin: admin@example.com / admin123
- User: user@example.com / user123

## 🖥️ Funcionalidades

### Usuario no autenticado
- Registrarse
- Iniciar sesión

### Usuario autenticado
- Ver lista de eventos
- Filtrar eventos (ciudad, fecha, disponibilidad)
- Ver detalles de evento
- Reservar tickets
- Ver confirmación de reserva
- Cerrar sesión

### Administrador (adicional)
- Crear eventos
- Editar eventos
- Eliminar eventos

## 🐳 Dockerización

docker compose up --build

Servicios incluidos:
- frontend: React + Nginx

## 📝 Autor
Alex Pérez Soriano
https://www.linkedin.com/in/alexperezsoriano/

## 📅 Fecha
Septiembre 2026

## 📄 Licencia
Este proyecto fue desarrollado como prueba técnica.