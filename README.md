# 🚌 [Nombre de la App] – Registro de Servicios de Transporte

Aplicación sencilla para registrar, almacenar y consultar de forma digital los servicios de transporte que se prestan, reemplazando el registro manual en papel.

---

## 📌 Contexto y problema

Hasta ahora, la información de los servicios se registraba **en papel**. Esto generaba problemas frecuentes:

- Pérdida o deterioro de documentos.
- Datos incompletos, ilegibles o duplicados.
- Dificultad para buscar información histórica.
- Imposibilidad de generar reportes rápidos y confiables.
- Sin copias de respaldo.

## 🎯 Objetivo

Mejorar el almacenamiento de los datos mediante una aplicación **simple y directa** que centralice los servicios en una base de datos, garantizando que **no se pierdan**, sean **fáciles de consultar** y estén **respaldados**.

### Objetivos específicos

- Digitalizar el registro de los servicios de transporte.
- Centralizar los datos en una base de datos.
- Permitir búsquedas, filtros y reportes en segundos.
- Implementar copias de seguridad automáticas.

### Alcance

La app se centra **únicamente en los servicios que brinda**. Por simplicidad, **no incluye** inicio de sesión de usuarios ni gestión de conductores.

---

## ✨ Funcionalidades principales

| Módulo | Descripción |
|---|---|
| **Servicios** | Registrar, editar, consultar y cambiar el estado de cada servicio prestado. |
| **Vehículos** | Lista básica de los vehículos asignados a los servicios (placa, tipo, estado). |
| **Búsqueda y filtros** | Consulta por fecha, tipo de servicio, vehículo o estado. |
| **Reportes** | Exportación a PDF/Excel de los servicios en un rango de fechas. |
| **Respaldo** | Copias de seguridad automáticas de la base de datos. |

> ✏️ *Ajusta esta tabla según los servicios reales que ofrece tu organización.*

---

## 🏗️ Arquitectura

```
┌─────────────┐      ┌──────────────┐      ┌────────────────┐
│  Frontend   │ ───► │   Backend    │ ───► │  Base de datos │
│ (Web/Móvil) │ ◄─── │  (API REST)  │ ◄─── │                │
└─────────────┘      └──────────────┘      └────────────────┘
                                                   │
                                                   ▼
                                          Copias de seguridad
```

## 🛠️ Tecnologías

> Reemplaza con las que uses realmente.

- **Frontend:** [React / Flutter / HTML+CSS+JS]
- **Backend:** [Node.js / Python (Django, Flask) / Java / PHP]
- **Base de datos:** [PostgreSQL / MySQL / SQLite / Firebase]
- **Control de versiones:** Git + GitHub

---

## 🗄️ Modelo de datos (resumen)

Entidades principales:

- **Servicio** (id, fecha, hora, tipo_servicio, origen, destino, id_vehículo, estado, observaciones)
- **Vehículo** (id, placa, tipo, estado)

Relación clave: un **servicio** se realiza con un **vehículo**; un vehículo puede tener muchos servicios.

---

## 🚀 Instalación y puesta en marcha

### Requisitos previos

- [Node.js / Python / etc.] versión X o superior
- [Motor de base de datos] instalado
- Git

### Pasos

```bash
# 1. Clonar el repositorio
git clone https://github.com/usuario/nombre-del-proyecto.git
cd nombre-del-proyecto

# 2. Instalar dependencias
# (ejemplo con Node.js)
npm install

# 3. Configurar variables de entorno
cp .env.example .env
# Edita .env con los datos de tu base de datos

# 4. Crear la base de datos / ejecutar migraciones
npm run migrate

# 5. Iniciar la aplicación
npm start
```

### Variables de entorno (`.env`)

```env
DB_HOST=localhost
DB_PORT=5432
DB_NAME=transporte
DB_USER=usuario
DB_PASSWORD=contraseña
PORT=3000
```

---

## 📁 Estructura del proyecto

```
/
├── src/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   └── config/
├── public/
├── tests/
├── docs/
├── .env.example
├── package.json
└── README.md
```

---

## 💾 Respaldo de datos

- Copias de seguridad programadas (diaria o semanal) de la base de datos.
- Almacenamiento del respaldo en una ubicación distinta a la del servidor principal.

---

## 🗺️ Plan de trabajo (Roadmap)

- [ ] Definir los servicios y los datos que se deben registrar
- [ ] Diseño de la base de datos
- [ ] Prototipo de la interfaz
- [ ] Módulo de servicios (registro, edición, consulta)
- [ ] Módulo de vehículos
- [ ] Búsqueda, filtros y reportes
- [ ] Migración de los datos históricos en papel
- [ ] Copias de seguridad automáticas
- [ ] Pruebas y capacitación
- [ ] Puesta en producción

---

## 🤝 Contribuir

1. Haz un *fork* del proyecto.
2. Crea una rama: `git checkout -b feature/nueva-funcionalidad`
3. Haz *commit* de tus cambios: `git commit -m "Agrega nueva funcionalidad"`
4. Sube la rama: `git push origin feature/nueva-funcionalidad`
5. Abre un *Pull Request*.

## 👥 Equipo

| Nombre | Rol |
|---|---|
| Santiago Ocampo | Desarrollador |
| Katherin Ortega | Desarrollador |
| Duvan Tique | Desarrollador |
| María Paz Urrego | Desarrolladora |

## 📄 Licencia

Este proyecto está bajo la licencia [MIT / otra]. Consulta el archivo `LICENSE` para más detalles.

## 📬 Contacto

[Tu nombre] – [correo@ejemplo.com]
