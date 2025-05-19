# Estándares de Calidad en el Diseño de Software - Caso MasterBikes

## 🎯 Objetivo
Definir y aplicar estándares de calidad en el diseño del sistema MasterBikes, de acuerdo con los fundamentos de la ingeniería de software, para contribuir a la robustez, mantenibilidad, usabilidad y accesibilidad del sistema.

---

## 1. Principios de Diseño Aplicados

### ✅ Abstracción
- Se utiliza para modelar entidades clave del dominio: bicicletas, pedidos, clientes, técnicos.
- Cada microservicio abstrae una responsabilidad del negocio: autenticación, gestión de productos, pedidos, reportes.

### ✅ Cohesión y Acoplamiento
- Los microservicios están diseñados con **alta cohesión** (cada uno tiene una función clara) y **bajo acoplamiento** (interactúan vía REST y API Gateway).
- Por ejemplo, `Bicicletas-Service` gestiona reparaciones y stock sin depender directamente de `Pedidos-Service`.

### ✅ Descomposición y Modularidad
- Arquitectura basada en microservicios Spring Boot.
- Cada componente puede evolucionar de forma independiente y escalar según demanda.

### ✅ Encapsulación
- Cada microservicio encapsula su lógica y su base de datos (Oracle RDS), impidiendo accesos cruzados indebidos.

---

## 2. Diseño de Interfaz de Usuario (UI)

### 🧠 Enfoque UX (User Experience)
- La interfaz está pensada para clientes, vendedores, técnicos y supervisores.
- Se busca adaptar la experiencia a las habilidades y expectativas de cada tipo de usuario.

### 🛠️ Prototipado
- Se recomienda el uso de herramientas como **Figma** o **Balsamiq** para construir wireframes y mockups.
- Esto facilita la validación temprana de flujos clave como: arriendo de bicicletas, seguimiento de pedidos y carga de reportes.

---

## 3. Usabilidad

### 🔍 Evaluación Heurística (Jakob Nielsen)
El sistema debe cumplir con los siguientes principios:
- **Visibilidad del estado del sistema** (ej: estado del pedido).
- **Consistencia y estándares** en botones, navegación y formularios.
- **Prevención de errores** con validaciones de entrada y sugerencias.
- **Control y libertad del usuario**, permitiendo cancelar acciones.

> Se recomienda validar mediante **listas de chequeo heurísticas** en pruebas de usabilidad internas.

---

## 4. Accesibilidad (según WCAG)

### 🌐 Principios UI:

| Principio       | Aplicación en MasterBikes                                  |
|-----------------|-------------------------------------------------------------|
| Perceptibilidad | Uso de contrastes adecuados, texto alternativo en imágenes. |
| Operabilidad    | Soporte de navegación con teclado.                          |
| Comprensibilidad| Etiquetas claras en formularios y mensajes de error.        |
| Robustez        | Compatibilidad con lectores de pantalla y navegadores.      |

> Para cumplimiento se sugiere aplicar **WCAG 2.1 nivel AA** como estándar mínimo.

---

## 5. Conclusiones

- El diseño modular, cohesivo y accesible de MasterBikes facilita la **escalabilidad**, **mantenibilidad** y **usabilidad** del sistema.
- Se recomienda continuar aplicando principios de **ingeniería de software** en etapas futuras, reforzando con **evaluaciones de interfaz y pruebas con usuarios reales**.

---
