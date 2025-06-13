# TodoList_Valverde_Nick
## Descripción General

El proyecto **TodoList_Valverde_Nick** es una aplicación web desarrollada utilizando el framework Spring Boot, orientada a la gestión de tareas (to-do list). El objetivo principal es permitir a los usuarios crear, visualizar, actualizar y eliminar tareas de manera eficiente, aplicando principios de desarrollo ágil y buenas prácticas de ingeniería de software.

## Arquitectura y Tecnologías

La aplicación sigue una arquitectura basada en capas, separando claramente la lógica de presentación, negocio y acceso a datos. Las tecnologías y herramientas principales utilizadas son:

- **Spring Boot**: Framework principal para el desarrollo de la aplicación backend.
- **Spring Data JPA**: Para la gestión de la persistencia de datos y la interacción con la base de datos.
- **H2 Database**: Base de datos en memoria utilizada para pruebas y desarrollo.
- **Thymeleaf**: Motor de plantillas para la generación dinámica de vistas HTML.
- **Maven**: Herramienta de gestión de dependencias y construcción del proyecto.
- **Lombok**: Para reducir la escritura de código repetitivo (getters, setters, constructores).
- **JUnit y Mockito**: Para la implementación de pruebas unitarias y de integración.

## Funcionalidades Implementadas

### 1. Gestión de Tareas

- **Creación de tareas**: Los usuarios pueden añadir nuevas tareas proporcionando un título y una descripción. Se valida que los campos obligatorios estén completos antes de guardar la tarea.
- **Visualización de tareas**: Se muestra una lista de todas las tareas almacenadas, permitiendo al usuario ver el estado actual de cada una.
- **Actualización de tareas**: Es posible modificar los detalles de una tarea existente, como el título, la descripción o el estado (pendiente/completada).
- **Eliminación de tareas**: Los usuarios pueden eliminar tareas de la lista, lo que elimina el registro correspondiente en la base de datos.

### 2. Persistencia de Datos

Se utiliza Spring Data JPA para mapear las entidades de dominio (Tarea) a tablas en la base de datos H2. Los repositorios permiten realizar operaciones CRUD de manera sencilla y eficiente.

### 3. Interfaz de Usuario

La interfaz de usuario está construida con Thymeleaf, permitiendo la renderización dinámica de las vistas y la interacción fluida con el backend. Se implementan formularios para la creación y edición de tareas, así como botones para eliminar y marcar tareas como completadas.

### 4. Validación y Manejo de Errores

Se implementan validaciones tanto del lado del cliente como del servidor para asegurar la integridad de los datos. Los mensajes de error se muestran de manera clara en la interfaz cuando ocurre alguna validación fallida.

### 5. Pruebas

El proyecto incluye pruebas unitarias para los servicios y pruebas de integración para los controladores, utilizando JUnit y Mockito. Esto garantiza que las funcionalidades principales se comporten según lo esperado y facilita el mantenimiento del código.

## Estructura del Proyecto

El proyecto está organizado en los siguientes paquetes principales:

- **controller**: Contiene las clases que gestionan las peticiones HTTP y coordinan la interacción entre la vista y la lógica de negocio.
- **service**: Incluye la lógica de negocio y las operaciones sobre las entidades.
- **repository**: Define las interfaces para el acceso a datos utilizando Spring Data JPA.
- **model/entity**: Contiene las clases que representan las entidades del dominio (por ejemplo, Tarea).
- **templates**: Carpeta donde se encuentran las vistas Thymeleaf.
- **static**: Recursos estáticos como CSS y JavaScript.

## Buenas Prácticas y Metodologías Ágiles

Durante el desarrollo se aplicaron principios de metodologías ágiles, como la entrega incremental de funcionalidades, la integración continua y la retroalimentación constante. El código está documentado y estructurado para facilitar la colaboración y el mantenimiento.

Se utilizaron control de versiones con Git, permitiendo el seguimiento de cambios y la colaboración efectiva. Además, se priorizó la simplicidad y la claridad en la implementación, siguiendo el principio KISS (Keep It Simple, Stupid) y aplicando el patrón MVC (Modelo-Vista-Controlador).

## Despliegue y Ejecución

La aplicación puede ejecutarse localmente utilizando Maven y Spring Boot. Al iniciar, la base de datos H2 se configura automáticamente y se inicializa el esquema necesario. El acceso a la interfaz de usuario se realiza a través de un navegador web, permitiendo la gestión completa de las tareas.

## Conclusión

**TodoList_Valverde_Nick** es una solución robusta y escalable para la gestión de tareas, implementada siguiendo buenas prácticas de desarrollo y utilizando tecnologías modernas del ecosistema Java. El proyecto sirve como base para futuras extensiones, como la autenticación de usuarios, la integración con bases de datos externas o la implementación de una API REST para clientes móviles o frontends modernos.