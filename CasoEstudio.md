**Caso de Estudio: Desarrollo de un Sistema de Gestión para una Biblioteca Universitaria**

**1. Instrucciones**

**Inicio (10 minutos)**

**1. Presentación del Caso (5 minutos):**

**o   Contexto del Caso:**

- La biblioteca de una universidad necesita modernizar su sistema de gestión para mejorar la eficiencia y la satisfacción del usuario.

- Problemas actuales: pérdida de libros, dificultades en la búsqueda de materiales, largas colas para préstamos y devoluciones.

**o   Requisitos del Cliente:**

  - Gestión de Usuarios, Gestión de Libros, Préstamo y Devolución, Catálogo en Línea, Reportes y Estadísticas.

Vienen más adelante.

**o   Roles y Responsabilidades:**

  - Gestor de Proyecto, Analista, Diseñador, Tester.

**2.    Asignación de Equipos y Roles (5 minutos):**

o   Formar equipos de 3-4 integrantes.

o   Asignar roles dentro de cada equipo.

  > - Gestor de Proyecto: Fabián Lecaros

  > - Analista: Héctor Águila

  > - Diseñador: Franco Ruz

  > - Tester: Vicente Barrera

**Desarrollo (105 minutos)**

**Bloque 1: Fase de Requisitos (35 minutos)**

**1. Recolección de Requisitos (20 minutos):**

  o  El analista se reúne con el cliente (instructor o estudiante en el rol de bibliotecario jefe) para obtener detalles adicionales y clarificar requisitos.

  o Documentar los requisitos detallados.

**Requisitos Adicionales**

  - **Seguridad y autenticación:**

  >- Ingreso con correo y contraseña.

  >- Encriptación de datos sensibles.

**- Historial de préstamos:**

  >- Registro de libros solicitados y devueltos por cada usuario.

**- Gestión de multas:**

  >- Posibilidad de registrar sanciones por retrasos en la devolución.

**- Reporte de disponibilidad:**

  >- Indicar si un libro está prestado o disponible.

**- Exportación de informes:**

  >- Generación de reportes en PDF o Excel para control de inventario.

**- Búsqueda avanzada en el catálogo:**

  >- Filtros por título, autor, categoría y disponibilidad.

**- Registro de actividad del sistema:**

  >- Seguimiento de acciones realizadas por los bibliotecarios y administradores.

**2. Planificación (15 minutos):**

o    El gestor de proyecto organiza una reunión inicial para discutir los objetivos y el alcance del proyecto.

**- Objetivos:**

  >-Construir un sistema para al gestión de la biblioteca del DUOC Puerto Montt.

**Ambito:**

>  - El sistema va a permitir registrar la pérdida de libros.

>  - El sistema no va a evitar la pérdida o robo de libros.

>  - El sistema será gestionado por personas, no incluyendo robots que automatizen la entrega y recepción de libros.

**Alcance:**

>  - **Tareas:** Analisis de Requisitos, Reuniones, Ingresar libros a la BD, programar la aplicación, Testing.

>  - **Tiempo de Duración del proyecto:** 6 meses.

>  - **Recursos:** Computadores, Servidor, Hosting.

o    Utilizar Trello para planificar y asignar tareas basadas en los requisitos documentados.

**Bloque 2: Fase de Diseño (35 minutos)**

**1. Diseño Preliminar (20 minutos):**

  o El diseñador elabora el diseño preliminar del sistema, incluyendo la arquitectura, el modelo de datos, y los mockups de la interfaz de usuario (UI/UX).

  o Preparar diagramas UML necesarios (diagramas de casos de uso).

**2. Revisión y Ajustes (15 minutos):**

  o El gestor de proyecto coordina una revisión del diseño preliminar con el cliente para obtener feedback.

  o El diseñador ajusta el diseño según el feedback recibido.

**Bloque 3: Fase de Validación y Discusión en Plenario (35 minutos)**

**1. Validación del Diseño y Especificaciones (20 minutos):**

  o El tester desarrolla un plan de pruebas y casos de prueba basados en los requisitos documentados (sin ejecución real de pruebas).

  o Asegurar que todas las especificaciones cumplen con los requisitos del cliente.

**2. Preparación de la Entrega (5 minutos):**

  o El equipo prepara la presentación final del sistema al cliente.

  o Documentar las lecciones aprendidas y preparar el informe de cierre del proyecto.

**3. Presentación y Discusión en Plenario (10 minutos):**

  o Cada equipo presenta su solución al plenario.

  o Se realiza una sesión de retroalimentación de pares, intercambiando opiniones y críticas constructivas.



Cierre (10 minutos)

**Retroalimentación del Instructor (10 minutos):**

  o El docente proporciona feedback final, destacando los puntos fuertes y las áreas de mejora.

  o Cierre de la actividad y reflexión sobre las lecciones aprendidas.



**Entregables:**

  · Documento de especificaciones de requisitos.

  · Diseño del sistema (diagramas UML, mockups de UI/UX).

  · Plan de proyecto y cronograma.

  · Casos de prueba y reporte de pruebas.

  · Informe final del proyecto.



**Herramientas Sugeridas:**

·        **Trello:** Para la gestión de tareas y planificación.



**2.    Contexto del Caso**

La biblioteca de una universidad ha decidido modernizar su sistema de gestión para mejorar la eficiencia y la satisfacción del usuario. Actualmente, el sistema es manual y presenta diversos problemas, como la pérdida de libros, dificultades en la búsqueda de materiales y largas colas para préstamos y devoluciones.

**Requisitos del Cliente:**

El cliente (representado por un instructor o un estudiante en el rol de bibliotecario jefe) ha proporcionado los siguientes requisitos iniciales:

**1.      Gestión de Usuarios:**

·        Registro de nuevos usuarios (estudiantes, profesores, personal).

·        Actualización y eliminación de usuarios.

·        Gestión de permisos y roles de usuarios.

**2.      Gestión de Libros:**

·        Registro de nuevos libros.

·        Actualización y eliminación de libros.

·        Búsqueda de libros por título, autor, ISBN, y categoría.

**3.      Préstamo y Devolución:**

·        Registro de préstamos de libros.

·        Registro de devoluciones de libros.

·        Notificaciones automáticas de vencimiento de préstamo.

**4.      Catálogo en Línea:**

·        Consulta en línea del catálogo de libros disponibles.

·        Reserva en línea de libros.

**5.      Reportes y Estadísticas:**

·        Generación de reportes de libros más prestados.

·        Generación de reportes de usuarios activos.

·        Estadísticas sobre el uso del sistema.



**Roles y Responsabilidades:**

**1.  Gestor de Proyecto:**

·        Coordinar el equipo de desarrollo.

·        Planificar y asignar tareas.

·        Mantener comunicación con el cliente.

·        Asegurar que el proyecto se mantenga dentro del presupuesto y plazo acordado.

**2.  Analista:**

·        Recolectar y documentar requisitos detallados del cliente.

·        Realizar análisis de requisitos y elaborar el documento de especificaciones.

·        Identificar y resolver ambigüedades en los requisitos.

**3.  Diseñador:**

·        Crear el diseño del sistema, incluyendo la arquitectura y el modelo de datos.

·        Diseñar la interfaz de usuario y la experiencia de usuario (UI/UX).

·        Preparar diagramas UML (casos de uso, clases, secuencia).

**4.  Tester:**

·        Desarrollar y ejecutar casos de prueba.

·        Identificar y reportar errores y fallos.

·        Asegurar la calidad del software mediante pruebas funcionales y no funcionales.

**Dinámica del Juego de Roles:**

**1. Fase de Requisitos:**

·        El analista se reúne con el cliente para obtener detalles adicionales y clarificar requisitos.

·        El gestor de proyecto organiza una reunión inicial para discutir los objetivos y el alcance del proyecto.

·        El analista presenta el documento de especificaciones al equipo para su revisión.



**2.      Fase de Diseño:**

·        El diseñador elabora el diseño preliminar del sistema y lo presenta al equipo.

·        El gestor de proyecto coordina la revisión del diseño con el cliente.

·        El diseñador ajusta el diseño según el feedback recibido.

**3.      Fase de Implementación:**

·        Los desarrolladores (pueden ser otros estudiantes no mencionados específicamente en los roles) empiezan a construir el sistema basado en el diseño aprobado.

·        El gestor de proyecto monitorea el progreso y asegura la alineación con el plan de trabajo.

**4.      Fase de Pruebas:**

·        El tester desarrolla un plan de pruebas y casos de prueba basados en los requisitos.

·        El tester ejecuta las pruebas, reporta defectos y colabora con los desarrolladores para su resolución.

·        El gestor de proyecto asegura que todos los requisitos han sido probados y validados.

**5.      Fase de Entrega:**

·        El gestor de proyecto organiza una reunión de revisión final con el cliente.

·        El equipo presenta el sistema al cliente y recibe feedback.

·        El gestor de proyecto documenta las lecciones aprendidas y prepara el informe de cierre del proyecto.
