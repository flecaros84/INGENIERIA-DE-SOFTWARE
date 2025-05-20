# Modelo 4+1 Vistas Aplicado a los Diagramas UML de MasterBikes

---

## 1. Vista Lógica (Logical View)

- **Preocupación:**  
  La funcionalidad que el sistema proporciona a los usuarios finales y la estructura de las entidades del dominio.

- **Stakeholders:**  
  Diseñadores, Desarrolladores, Analistas.

- **Diagramas UML Pertinentes Proyecto MasterBikes:**
  - ✅ **Diagrama de Clases Principal (1):**  
    Muestra las principales clases del dominio (Usuario, Producto, Pedido, Arriendo, Reparacion, etc.), sus atributos y relaciones. Es la pieza central de esta vista.

  - ✅ **Diagramas de Estado (3):**
    - Estado de Arriendo
    - Estado de Reparación
    - Estado de Pedido (de Venta)
  
  - **Justificación:**  
    Estos diagramas permiten comprender en detalle el comportamiento dinámico y el ciclo de vida de los principales objetos del dominio, aspectos fundamentales de la lógica del sistema.  
    - *(Opcionalmente, también pueden incluirse aquí ciertos Diagramas de Secuencia, siempre que se centren en la colaboración entre objetos de dominio para implementar funcionalidades específicas, más que en la interacción entre componentes de alto nivel).*

---

## 2. Vista de Desarrollo (Development View) o Vista de Implementación

- **Aspectos Claves:**  
  La organización de los módulos de software, componentes y subsistemas en el entorno de desarrollo.
  Cómo se estructura el código fuente.

- **Stakeholders:**  
  Desarrolladores, Arquitectos de Software, Gestores de Configuración.

- **Diagramas UML Pertinentes de tu Proyecto:**
  - ✅ **Diagrama de Componentes (1):**  
    Muestra los principales componentes de software (FrontendWebApp, API Gateway, Microservicios como Auth-Service, Bicicletas-Service, etc., Bases de Datos lógicas) y sus dependencias e interfaces. Es el diagrama principal de esta vista.

---

## 3. Vista de Procesos (Process View)

- **Aspectos Claves:**  
  Los aspectos dinámicos del sistema en tiempo de ejecución, como la concurrencia, distribución, comunicación entre procesos/servicios, rendimiento y escalabilidad.

- **Stakeholders:**  
  Integradores de Sistemas, Arquitectos, Desarrolladores (para rendimiento y concurrencia).

- **Diagramas UML Pertinentes de tu Proyecto:**
  - ✅ **Diagramas de Secuencia (3):**
    - Registro de Venta
    - Cliente Solicita Reparación
    - Supervisor Registra Ingreso de Stock
    - **Justificación:**  
      Estos diagramas son cruciales aquí porque muestran cómo los diferentes componentes (especialmente los microservicios) interactúan en tiempo de ejecución, el orden de los mensajes y los flujos de comunicación para lograr una tarea.

  - ✅ **Diagramas de Actividad (3):**
    - Proceso de Solicitud y Gestión Inicial de Reparación
    - Proceso de Venta de Producto con Despacho
    - Proceso de Solicitud de Arriendo de Bicicleta
    - **Justificación:**  
      Aunque también pueden relacionarse con la Vista Lógica o de Escenarios, los diagramas de actividad que muestran el flujo de control a través de diferentes componentes o responsabilidades (carriles) también ilustran aspectos de los procesos del sistema. Particularmente si muestran puntos de sincronización o paralelismo (aunque no los hemos detallado mucho así).

---

## 4. Vista Física (Physical View) o Vista de Despliegue

- **Aspectos Claves:**  
  El mapeo del software a los elementos de hardware o infraestructura de despliegue. Cómo se distribuyen los componentes de software en la infraestructura física o virtual.

- **Stakeholders:**  
  Ingenieros de Sistemas, Administradores de Sistemas, Personal de Operaciones, Arquitectos de Infraestructura.

- **Diagramas UML Pertinentes de tu Proyecto:**
  - ✅ **Diagrama de Despliegue (1):**  
    Muestra cómo los artefactos de software (JARs de microservicios, frontend, base de datos) se despliegan en nodos de infraestructura (Navegador Cliente, Servidores EC2, Servidor RDS AWS, Sistema Externo SHIMANO). Es el diagrama principal de esta vista.

---

## +1. Vista de Escenarios (Scenarios View) o Vista de Casos de Uso

- **Aspectos Claves:**  
  Ilustrar y validar el diseño arquitectónico utilizando un conjunto de casos de uso o escenarios clave. Demuestra que las otras 4 vistas trabajan juntas para cumplir con los requisitos funcionales.

- **Stakeholders:**  
  Todos, incluyendo Clientes (del proyecto), Analistas, Testers, Arquitectos.

- **Diagramas UML Pertinentes de tu Proyecto:**
  - ✅ **Diagramas de Casos de Uso (3):**
    - Interacciones del Cliente
    - Interacciones del Personal Interno (Técnico y Vendedor)
    - Supervisor e Integraciones del Sistema
    - **Justificación:**  
      Estos son la representación directa de los escenarios y funcionalidades clave desde la perspectiva de los actores. Son la base para esta vista.

  - **Apoyo de otros diagramas:**  
    Los Diagramas de Secuencia y los Diagramas de Actividad sirven como complemento a los Diagramas de Casos de Uso, ya que permiten detallar cómo se desarrollan los escenarios principales del sistema. Al entender esta vista, podemos mostrar cómo cada caso de uso se lleva a cabo paso a paso: los diagramas de secuencia ayudan a ilustrar la interacción entre los actores y los distintos componentes, mientras que los diagramas de actividad muestran el flujo de acciones y decisiones que intervienen en cada proceso. De esta manera, se obtiene una visión más clara y completa de cómo se cumplen los requisitos funcionales en la práctica.

---

## Estructura para la Presentación

Al presentar o documengtar la arquitectura usando el modelo 4+1, podremos tener una sección para cada vista:

1. **Introducción al Modelo 4+1 Vistas**  
   El Modelo 4+1 es un enfoque para describir la arquitectura de software usando cinco vistas complementarias: lógica, de procesos, de desarrollo, física y de casos de uso. Cada vista aborda diferentes preocupaciones de los interesados, facilitando la comprensión y comunicación del sistema.

2. **Vista Lógica**
   - Descripción de la vista.
   - Diagrama de Clases Principal (y explicación).
   - Diagramas de Estado (Arriendo, Reparación, Pedido) (y explicación de cada uno).

3. **Vista de Desarrollo**
   - Descripción de la vista.
   - Diagrama de Componentes (y explicación).

4. **Vista de Procesos**
   - Descripción de la vista.
   - Diagramas de Secuencia (Venta, Solicitud Reparación, Ingreso Stock) (y explicación de cada uno).
   - Diagramas de Actividad (Solicitud Reparación, Venta con Despacho, Arriendo) (y explicación, destacando el flujo de control).

5. **Vista Física**
   - Descripción de la vista.
   - Diagrama de Despliegue (y explicación).

6. **Vista de Escenarios (Casos de Uso)**
   - Descripción de la vista.
   - Diagramas de Casos de Uso (Cliente, Personal Interno, Supervisor) (y explicación de cada uno).
   - Mencionar cómo los diagramas de secuencia y actividad seleccionados ilustran la realización de estos casos de uso.
  