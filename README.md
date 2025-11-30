Taller ASP.NET Core - Sistema de Gestión de Tareas
Este repositorio contiene el proyecto desarrollado durante el webinar "Uso de ASP.NET Core" realizado en la Semana de Ingeniería 2025. Se implementa una aplicación web completa para la gestión de listas de tareas personalizadas utilizando el patrón Modelo-Vista-Controlador (MVC).

Descripción del Proyecto
El sistema permite a los usuarios registrarse, iniciar sesión y gestionar sus propias listas de tareas de manera personalizada. Cada usuario tiene acceso exclusivo a sus tareas, las cuales puede crear, visualizar, actualizar, eliminar y organizar según sus necesidades.
Este proyecto fue desarrollado como parte de la asignación del taller de ASP.NET Core, demostrando la implementación práctica de conceptos clave del desarrollo web moderno con tecnologías .NET.

Características Principales

Aplicación web construida con ASP.NET Core MVC
Sistema de autenticación de usuarios (cada usuario accede a su cuenta personal)
Gestión de listas de tareas personalizadas por usuario
Funcionalidades CRUD completas:

Crear nuevas tareas
Leer y visualizar todas las tareas
Actualizar tareas existentes
Eliminar tareas completadas o no deseadas


Filtrado y ordenamiento de tareas por prioridad
Seguridad: Cada usuario solo puede ver y gestionar sus propias tareas
Diseño responsivo adaptable a dispositivos móviles y escritorio


Tecnologías Utilizadas
TecnologíaDescripciónASP.NET Core 7.0+Framework principal para el desarrollo webEntity Framework CoreORM para la gestión de base de datosSQL Server / SQLiteBase de datos para almacenamiento persistenteIdentity FrameworkSistema de autenticación y autorizaciónBootstrap 5Framework CSS para diseño responsivoRazor PagesMotor de vistas para las páginas webC#Lenguaje de programación del lado del servidor

Requisitos Previos
Antes de ejecutar el proyecto, asegúrate de tener instalado:

.NET SDK 7.0 o superior
Visual Studio 2022 o Visual Studio Code
SQL Server (o SQL Server Express) / SQLite
Git para clonar el repositorio


Instrucciones para Ejecutar el Proyecto
1. Clonar el Repositorio
bashgit clone https://github.com/Emanuel-Izaguirre-Cortes-03/Taller-ASP.NET-Core.git
cd Taller-ASP.NET-Core
2. Abrir el Proyecto

Opción A: Abre la solución (.sln) en Visual Studio 2022
Opción B: Abre la carpeta del proyecto en Visual Studio Code

3. Configurar la Base de Datos
a) Configurar la cadena de conexión
Edita el archivo appsettings.json y actualiza la cadena de conexión según tu entorno:
json{
  "ConnectionStrings": {
    "DefaultConnection": "Server=(localdb)\\mssqllocaldb;Database=TallerASPNETCore;Trusted_Connection=True;MultipleActiveResultSets=true"
  }
}
Para SQL Server:
json"DefaultConnection": "Server=localhost;Database=TallerASPNETCore;User Id=tu_usuario;Password=tu_contraseña;"
Para SQLite (más simple):
json"DefaultConnection": "Data Source=tareas.db"
b) Aplicar las migraciones
Ejecuta los siguientes comandos en la terminal:
bashdotnet ef migrations add InitialCreate
dotnet ef database update
Nota: Si no tienes dotnet-ef instalado, ejecuta primero:
bashdotnet tool install --global dotnet-ef
4. Ejecutar la Aplicación
bashdotnet run
O presiona F5 en Visual Studio para ejecutar en modo debug.
5. Acceder a la Aplicación
Abre tu navegador y visita:

HTTP: http://localhost:5000
HTTPS: https://localhost:5001


Estructura del Proyecto
Taller-ASP.NET-Core/
│
├── Controllers/           # Controladores MVC (lógica de negocio)
│   ├── HomeController.cs
│   ├── TareasController.cs
│   └── AccountController.cs
│
├── Models/               # Modelos de datos (entidades)
│   ├── Tarea.cs
│   ├── Usuario.cs
│   └── ApplicationDbContext.cs
│
├── Views/                # Vistas Razor (interfaz de usuario)
│   ├── Home/
│   ├── Tareas/
│   ├── Account/
│   └── Shared/
│
├── wwwroot/              # Recursos estáticos
│   ├── css/             # Archivos CSS
│   ├── js/              # Archivos JavaScript
│   └── lib/             # Bibliotecas de terceros
│
├── Data/                 # Configuración de base de datos
│   └── Migrations/
│
├── appsettings.json      # Configuración de la aplicación
├── Program.cs            # Punto de entrada de la aplicación
└── README.md             # Este archivo

Credenciales de Prueba
Para facilitar la evaluación del proyecto, puedes usar las siguientes credenciales:
Usuario de demostración:

Email: demo@correo.com
Contraseña: Demo123!

O registra tu propio usuario en la página de registro.

Funcionalidades Implementadas
1. Sistema de Autenticación

Registro de nuevos usuarios
Inicio de sesión seguro
Cierre de sesión
Protección de rutas (solo usuarios autenticados pueden acceder)

2. Gestión de Tareas (CRUD)

Crear: Formulario para agregar nuevas tareas con título, descripción y prioridad
Leer: Visualización de todas las tareas del usuario
Actualizar: Edición de tareas existentes
Eliminar: Eliminación de tareas con confirmación

3. Características Adicionales

Filtrado de tareas por prioridad (Alta, Media, Baja)
Ordenamiento de tareas
Marcado de tareas como completadas
Interfaz intuitiva y fácil de usar


Capturas de Pantalla
Página de Inicio
Vista principal de la aplicación con las tareas del usuario
Formulario de Creación
Interfaz para agregar nuevas tareas
Sistema de Filtros
Opciones para organizar y filtrar tareas

Contexto Académico
Materia: Desarrollo de Aplicaciones Web
Evento: Webinar "Uso de ASP.NET Core" - Semana de Ingeniería 2025
Institución: [Tu institución educativa]
Estudiante: Emanuel Izaguirre Cortés

Criterios de Evaluación Cumplidos

Aplicación web funcional con ASP.NET Core y patrón MVC
Sistema de autenticación de usuarios implementado
Cada usuario tiene su lista de tareas personalizada
Funcionalidades CRUD completas (Crear, Leer, Actualizar, Eliminar)
Filtrado por prioridad y ordenamiento
Proyecto completo subido a repositorio público en GitHub
README con descripción detallada del proyecto


Contribuciones
Este proyecto fue desarrollado con fines académicos. Si deseas hacer sugerencias o mejoras:

Haz un Fork del proyecto
Crea una rama para tu feature (git checkout -b feature/MejoraNueva)
Commit tus cambios (git commit -m 'Agrega nueva mejora')
Push a la rama (git push origin feature/MejoraNueva)
Abre un Pull Request


Contacto
Emanuel Izaguirre Cortés
GitHub: @Emanuel-Izaguirre-Cortes-03

Licencia
Este proyecto se distribuye bajo la Licencia MIT. Consulta el archivo LICENSE para más detalles.

Agradecimientos

Gracias a los instructores del webinar "Uso de ASP.NET Core"
A la comunidad de .NET y ASP.NET Core por la documentación y recursos
A Microsoft por proporcionar herramientas de desarrollo de calidad
