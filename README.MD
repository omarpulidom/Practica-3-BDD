# Decisión de Tecnologías

En esta sección se explican las decisiones tecnológicas tomadas para el desarrollo del sistema, justificando la elección de la base de datos, la plataforma de hosting y el stack tecnológico utilizado.

---

## 1. Base de Datos

Para el desarrollo del sistema se eligió **PostgreSQL** como base de datos principal.

La razón principal de esta decisión es que la aplicación está diseñada para el contexto de **una clínica médica**, donde los datos tienen **relaciones claras y estructuradas** entre distintas entidades. Por ejemplo:

* Pacientes
* Doctores
* Citas médicas
* Historial clínico
* Recetas médicas

Estas entidades requieren **relaciones bien definidas**, como por ejemplo:

* Un paciente puede tener muchas citas.
* Una cita pertenece a un doctor y a un paciente.
* Un historial clínico pertenece a un paciente.

Las bases de datos relacionales como PostgreSQL permiten manejar este tipo de estructuras mediante:

* **Claves foráneas**
* **Integridad referencial**
* **Transacciones seguras**
* **Consultas complejas con SQL**

Esto es especialmente importante en sistemas médicos, donde **la consistencia y la confiabilidad de los datos son críticas**.

Además, PostgreSQL ofrece ventajas importantes como:

* Alto rendimiento en consultas complejas
* Gran estabilidad en aplicaciones en producción
* Amplio soporte en frameworks modernos

Se consideró el uso de **MongoDB**, pero se descartó porque es una base de datos **NoSQL orientada a documentos**, más adecuada para datos semiestructurados o altamente flexibles. En el caso de esta aplicación, la estructura de los datos es **estable y relacional**, por lo que PostgreSQL resulta una opción más adecuada.

---

## 2. Plataforma de Hosting

Para el despliegue de la aplicación se eligió **PythonAnywhere** como plataforma de hosting.

La principal razón es que el proyecto está desarrollado completamente en **Python**, y PythonAnywhere es una plataforma optimizada específicamente para aplicaciones basadas en este lenguaje.

Entre las ventajas que encontramos destacan:

* **Soporte nativo para aplicaciones Python**
* Facilidad para desplegar aplicaciones web
* Configuración sencilla para entornos virtuales
* Integración directa con frameworks de Python
* Panel de control simple para gestionar procesos y logs

Otra ventaja importante es que permite **configurar rápidamente aplicaciones basadas en frameworks modernos**, lo que facilita el proceso de despliegue y mantenimiento.

También se evaluó el uso de **Render**, ya que es una plataforma moderna de despliegue en la nube. Sin embargo, PythonAnywhere resultó más conveniente para este proyecto debido a:

* su enfoque específico en aplicaciones Python,
* una configuración más directa para proyectos pequeños o académicos,
* y un proceso de despliegue más simple.

Esto permitió concentrarnos más en el desarrollo de la aplicación y menos en la configuración de infraestructura.

---

## 3. Stack Tecnológico

El sistema fue desarrollado utilizando un stack tecnológico basado principalmente en el lenguaje **Python** y el framework **FastAPI**.

### Lenguaje de programación

Se eligió Python debido a varias razones:

* Sintaxis clara y fácil de mantener
* Amplio ecosistema de librerías
* Gran popularidad en desarrollo backend
* Excelente soporte para APIs y aplicaciones web

Además, el equipo tiene experiencia trabajando con Python, lo que permitió acelerar el desarrollo del proyecto.

---

### Framework Backend

El framework principal utilizado es **FastAPI**.

FastAPI es un framework moderno para construir APIs con Python que ofrece múltiples ventajas:

* **Alto rendimiento**, comparable con frameworks de otros lenguajes
* **Soporte nativo para asincronía**
* **Documentación automática de la API**
* **Validación automática de datos**
* **Fácil integración con bases de datos y librerías externas**

Otra ventaja importante es que FastAPI genera automáticamente documentación interactiva mediante **Swagger UI**, lo que facilita probar y entender los endpoints de la API durante el desarrollo.

Además, FastAPI permite construir aplicaciones **escalables y modulares**, lo cual es importante para proyectos que pueden crecer en el futuro.

---

## Conclusión

Las tecnologías seleccionadas permiten construir una aplicación **robusta, escalable y mantenible**.

* **PostgreSQL** proporciona una base sólida para manejar datos relacionales complejos dentro del contexto médico.
* **PythonAnywhere** facilita el despliegue de aplicaciones desarrolladas en Python sin requerir configuraciones complejas.
* **FastAPI** ofrece una forma moderna, rápida y eficiente de desarrollar APIs backend.

En conjunto, este stack tecnológico permite desarrollar un sistema confiable y adaptable a futuras ampliaciones del proyecto.
