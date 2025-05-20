# Textos Introductorios para los Diagramas (Modelo 4+1 Vistas)

## Vista de Escenarios (+1) (Casos de Uso)

### Diagrama de Casos de Uso 01: Interacciones del Cliente

> Comenzaremos explorando las funcionalidades clave desde la perspectiva del usuario final. Este diagrama de Casos de Uso ilustra las principales interacciones que un Cliente puede realizar con el sistema MasterBikes, desde registrarse y solicitar servicios como arriendos o reparaciones, hasta consultar su historial y recibir promociones.

### Diagrama de Casos de Uso 02: Interacciones del Personal Interno (Técnico y Vendedor)

> A continuación, nos enfocamos en los roles operativos internos. Este diagrama detalla los Casos de Uso para el Técnico, centrado en la gestión de reparaciones y consulta de piezas, y para el Vendedor, enfocado en el registro de ventas, consulta de stock de productos y gestión de despachos.

### Diagrama de Casos de Uso 03: Supervisor e Integraciones del Sistema

> Este diagrama presenta los Casos de Uso del Supervisor, quien se encarga de la generación de reportes, la visualización de indicadores y la gestión administrativa del stock. Además, ilustra cómo el sistema MasterBikes interactúa con sistemas externos, como la API de SHIMANO, para consultas de stock de proveedores.

---

## Vista Lógica

### Diagrama de Clases Principal: Dominio MasterBikes

> Para entender la estructura fundamental de la información que maneja MasterBikes, presentamos el Diagrama de Clases principal. Este diagrama identifica las entidades de negocio clave del sistema, como Usuarios, Productos, Pedidos, Arriendos y Reparaciones, junto con sus atributos más importantes y las relaciones que existen entre ellas.

### Diagrama de Estado: Ciclo de Vida de un Arriendo

> Un objeto "Arriendo" pasa por diversas etapas desde su solicitud hasta su finalización. Este Diagrama de Estado detalla los diferentes estados de un arriendo – como Solicitado, Confirmado, Activo o Finalizado – y los eventos o acciones que provocan las transiciones entre ellos, incluyendo el manejo de pagos o multas.

### Diagrama de Estado: Ciclo de Vida de una Reparación

> El proceso de una "Reparación" también tiene un ciclo de vida complejo. Este diagrama ilustra los estados por los que pasa una solicitud de reparación, desde que es Solicitada, pasando por la Evaluación, Espera de Repuestos, En Reparación, hasta su culminación como Entregada, Cancelada o incluso No Reparable.

### Diagrama de Estado: Ciclo de Vida de un Pedido de Venta

> Finalmente, para las ventas de productos, el Diagrama de Estado del "Pedido" muestra su evolución. Detallamos los estados desde que el pedido es Creado, pasando por la confirmación de pago y stock, su preparación, el tránsito del envío, hasta ser Entregado al cliente o, alternativamente, Cancelado.

---

## Vista de Desarrollo (o Implementación)

### Diagrama de Componentes: Sistema MasterBikes

> Desde la perspectiva de la organización del software, este Diagrama de Componentes ilustra los principales bloques de construcción de MasterBikes. Se identifican el Frontend, el API Gateway, cada uno de los microservicios especializados (como Auth-Service, Bicicletas-Service, etc.) y la capa de persistencia, mostrando sus dependencias e interfaces principales.

---

## Vista de Procesos

### Diagrama de Secuencia: Registro de Venta en MasterBikes

> Para entender cómo los componentes colaboran en tiempo real, este Diagrama de Secuencia detalla la interacción cronológica de mensajes para el proceso de "Registro de una Venta". Muestra cómo el Frontend, a través del API Gateway, interactúa con Pedidos-Service y Bicicletas-Service para validar stock, crear el pedido y notificar al cliente.

### Diagrama de Secuencia: Cliente Solicita Reparación de Bicicleta

> Este Diagrama de Secuencia ilustra el flujo de mensajes cuando un "Cliente Solicita una Reparación". Detallamos la comunicación desde la interfaz de usuario, pasando por el API Gateway, hasta el Bicicletas-Service que registra la solicitud, y el Notificaciones-Service que confirma la recepción al cliente.

### Diagrama de Secuencia: Supervisor Registra Ingreso de Stock Físico

> La gestión de inventario es crucial. Este Diagrama de Secuencia muestra el proceso cuando un "Supervisor Registra un Ingreso de Stock". Se visualiza la interacción con la interfaz de administración, el API Gateway y el Bicicletas-Service para actualizar las cantidades de inventario.

### Diagrama de Actividad: Proceso de Solicitud de Reparación

> Cambiando a una perspectiva de flujo de trabajo, este Diagrama de Actividad modela el "Proceso de Solicitud de Reparación". Utiliza carriles para mostrar las responsabilidades del Cliente, la Interfaz de Usuario, Bicicletas-Service y Notificaciones-Service, detallando las acciones y decisiones desde la solicitud inicial hasta la confirmación.

### Diagrama de Actividad: Proceso de Venta de Producto con Despacho

> Este Diagrama de Actividad ilustra el flujo completo de una "Venta de Producto con Despacho". Se detallan las actividades y responsabilidades de los diferentes actores y servicios del sistema, desde la selección del producto por el cliente, la verificación de stock, la creación del pedido, hasta la gestión y notificación de las etapas del despacho.

### Diagrama de Actividad: Proceso de Solicitud de Arriendo de Bicicleta

> Finalmente, en cuanto a actividades, este diagrama muestra el "Proceso de Solicitud de Arriendo de Bicicleta". Describe el flujo de acciones del cliente y del sistema, incluyendo la selección, la verificación de disponibilidad, el registro del arriendo y la confirmación enviada al cliente.

---

## Vista Física (o de Despliegue)

### Diagrama de Despliegue: Sistema MasterBikes

> Para comprender cómo se distribuye físicamente nuestro sistema, este Diagrama de Despliegue muestra los nodos de infraestructura y cómo los artefactos de software (como los microservicios y la base de datos) se despliegan en ellos. Se ilustra el uso de la nube de AWS, con instancias EC2 para los servicios y RDS para la base de datos Oracle.
