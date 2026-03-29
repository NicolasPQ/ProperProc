<div align="center">
  <h1>🛒 Proper Proc</h1>
  <p>Sistema de Gestión Web para el Bazar Plásticos y Envases Descartables "NENO"</p>

  ![ASP.NET Core](https://img.shields.io/badge/ASP.NET_Core-MVC-512BD4?style=flat-square&logo=dotnet)
  ![C#](https://img.shields.io/badge/C%23-Backend-239120?style=flat-square&logo=csharp)
  ![SQL Server](https://img.shields.io/badge/SQL_Server-Database-CC2927?style=flat-square&logo=microsoftsqlserver)
  ![SignalR](https://img.shields.io/badge/SignalR-WebSockets-FF6B00?style=flat-square)
  ![JWT](https://img.shields.io/badge/JWT-Auth-000000?style=flat-square&logo=jsonwebtokens)
  ![Scrum](https://img.shields.io/badge/Scrum-Agile-6DB33F?style=flat-square)
</div>

---

## 📌 Sobre el Proyecto

**Proper Proc** es un sistema de gestión web desarrollado como Proyecto de Grado para la
Universidad de Aquino Bolivia (UDABOL), orientado a digitalizar y optimizar los procesos
operativos del Bazar Plásticos y Envases Descartables "NENO", ubicado en la zona de la Ramada,
Santa Cruz de la Sierra – Bolivia.

El sistema reemplazó un manejo completamente manual (libros diarios, registros en papel,
cotizaciones físicas) por una plataforma centralizada con control de acceso por roles, punto de
venta, gestión de inventario y reportes analíticos en tiempo real.

> ⚠️ Este repositorio es de carácter público con fines de presentación. El código fuente completo
> está disponible en el repositorio privado del proyecto.

---

## 🖥️ Capturas del Sistema

### 🔐 Autenticación
<!-- Imagen: pantalla de inicio de sesión -->
![Login](./screenshots/login.png)

---

### 👥 Módulo de Administración
Gestión de usuarios, empleados, asistencias, roles y permisos, y bitácora de actividad.

<!-- Imagen: panel de usuarios / empleados / roles -->
![Administración](./screenshots/modulo_administracion.png)

---

### 📦 Módulo de Configuración
Catálogo de productos con precios en BOB/USD, generación de códigos de barras, categorías y
gestión de archivos.

<!-- Imagen: listado de productos / catálogo -->
![Configuración](./screenshots/modulo_configuracion.png)

---

### 🛒 Módulo de Ventas
Punto de venta con múltiples ventas simultáneas, escaneo de códigos de barras, cobros en BOB/USD,
generación de notas de venta y gestión de cuentas por cobrar.

<!-- Imagen: punto de venta en acción -->
![Ventas](./screenshots/modulo_ventas.png)

---

### 📋 Módulo de Compras
Generación de cotizaciones, exportación en PDF y texto, confirmación de compras, cuentas por
pagar y gestión de proveedores.

<!-- Imagen: panel de cotizaciones o compras -->
![Compras](./screenshots/modulo_compras.png)

---

### 💰 Módulo de Caja
Apertura y cierre de caja con conteo de fraccionamiento (billetes/monedas), movimientos
financieros, ingresos y egresos, métodos de pago configurables y tipo de cambio histórico.

<!-- Imagen: panel de caja / cierre de caja -->
![Caja](./screenshots/modulo_caja.png)

---

### 📊 Módulo de Reportes & Dashboard
Dashboard de rendimiento en **tiempo real** vía WebSockets (SignalR). Reportes exportables en
PDF y Excel: ventas, compras, asistencias, tendencias de mercado, movimientos de caja y
comparativa financiera.

<!-- Imagen: dashboard o reporte de ventas -->
![Reportes](./screenshots/modulo_reportes.png)

---

## 🏗️ Arquitectura

El sistema implementa una arquitectura de **5 capas** con patrón MVC:

| Capa          | Descripción                                                                  |
|---------------|------------------------------------------------------------------------------|
| Presentación  | ASP.NET Core MVC – vistas Razor, controladores, middlewares y sesiones JWT   |
| API           | API REST en ASP.NET Core – endpoints, SignalR hubs, autenticación JWT        |
| Negocios      | Servicios, validaciones, reglas de negocio y utilidades (encriptación)       |
| Datos         | Repositorios, interfaces, DTOs y contexto de EF Core                         |
| Dominio       | Entidades que mapean las tablas de la base de datos (Code First)              |

<!-- Imagen: diagrama de arquitectura de capas -->
![Arquitectura](./screenshots/arquitectura.png)

---

## 🗄️ Modelo de Base de Datos

<!-- Imagen: diagrama lógico de la base de datos (Oracle Data Modeler) -->
![Base de Datos](./screenshots/diagrama_bd.png)

---

## 🛠️ Stack Tecnológico

| Categoría            | Tecnología                          |
|----------------------|-------------------------------------|
| Lenguaje             | C# (.NET Core 6+)                   |
| Frontend             | ASP.NET Core MVC, Razor Views       |
| Backend / API        | ASP.NET Core REST API               |
| Base de Datos        | Microsoft SQL Server 2019+          |
| ORM                  | Entity Framework Core               |
| Tiempo Real          | SignalR (WebSockets)                |
| Autenticación        | JSON Web Tokens (JWT) + RBAC        |
| Control de Versiones | Git & GitHub                        |
| Metodología          | Scrum (6 sprints, Planning Poker)   |
| IDE                  | Visual Studio 2022                  |
| Gestión de Proyecto  | Trello                              |
| Modelado             | draw.io, Oracle SQL Data Modeler    |

---

## 📋 Módulos del Sistema
```
Proper Proc
├── 🔐 Autenticación y Seguridad   (JWT, RBAC, Bitácora)
├── 👥 Administración              (Usuarios, Empleados, Asistencias, Roles)
├── 📦 Configuración               (Productos, Categorías, Archivos, Códigos de barras)
├── 🛒 Ventas                      (POS, Clientes, Cuentas por Cobrar)
├── 📋 Compras                     (Cotizaciones, Proveedores, Cuentas por Pagar)
├── 💰 Caja                        (Apertura/Cierre, Movimientos, Métodos de Pago, T/C)
└── 📊 Reportes                    (Dashboard en tiempo real, PDF/Excel)
```

---

## 📐 Metodología

El proyecto fue desarrollado utilizando **Scrum**, con 6 sprints de duración variable
(5 a 21 días), estimados mediante **Planning Poker** y un total de **382 puntos de historia**
a lo largo de **82 días de desarrollo**. El desempeño de cada sprint fue monitoreado con
**Burndown Charts**.

---

## 👨‍💻 Autor

**Nicolas Parada Quevedo**  
Ingeniería de Sistemas – Universidad de Aquino Bolivia (UDABOL)  
Santa Cruz de la Sierra, Bolivia · 2026

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Nicolas_Parada-0A66C2?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/nicolas-parada-quevedo-227337274)
[![GitHub](https://img.shields.io/badge/GitHub-NicolasPQ-181717?style=flat-square&logo=github)](https://github.com/NicolasPQ)
