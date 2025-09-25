# Descripción del POM y su Documentación

Tu archivo `pom.xml` es la configuración principal de tu proyecto Maven. Contiene información vital sobre sus dependencias, cómo debe ser compilado y empaquetado, y qué plugins debe utilizar. La documentación es crucial para que otros desarrolladores entiendan rápidamente el propósito de cada parte de la configuración.

## Dependencias

Aquí tienes una lista de las dependencias de tu proyecto con una breve descripción de cada una:


- **spring-boot-starter-web**: Incluye todo lo necesario para construir aplicaciones web y APIs RESTful, como Spring MVC y un servidor web embebido.


- **spring-boot-starter-validation**: Habilita la validación de datos de entrada en tus endpoints utilizando la especificación de Jakarta Bean Validation.


- **spring-boot-starter-actuator**: Proporciona endpoints de monitoreo y gestión para la aplicación en producción.


- **spring-boot-starter-data-jpa**: Permite la interacción con bases de datos relacionales a través de Spring Data JPA.


- **com.h2database**: Una base de datos en memoria liviana, ideal para el desarrollo y las pruebas.


- **lombok**: Reduce el código repetitivo (como getters y setters) a través de anotaciones, manteniendo el código limpio.


- **mapstruct**: Un generador de código que crea mappers de Java seguros y eficientes para transferir datos entre objetos.


- **spring-boot-devtools**: Ofrece herramientas de desarrollo útiles, como el reinicio automático de la aplicación.


- **springdoc-openapi-starter-webmvc-ui**: Genera automáticamente la documentación de la API (Swagger), proporcionando una interfaz de usuario interactiva para probar los endpoints.


- **spring-boot-starter-hateoas**: Permite construir APIs que siguen el principio HATEOAS, añadiendo enlaces a los recursos para facilitar la navegación.


- **spring-cloud-starter-netflix-eureka-client**: Habilita el registro del servicio en un servidor Eureka para el descubrimiento de microservicios.


- **spring-boot-starter-test**: Proporciona las librerías necesarias para escribir pruebas unitarias y de integración.


- **spring-restdocs-mockmvc**: Permite generar documentación a partir de tus pruebas, asegurando que siempre esté actualizada.

## Plugins

Estos plugins son cruciales para el ciclo de vida de tu proyecto:


- **maven-compiler-plugin**: Este plugin compila el código fuente del proyecto. La configuración es vital, ya que `annotationProcessorPaths` se encarga de ejecutar Lombok y MapStruct antes de la compilación, asegurando que el código generado esté disponible.


- **jacoco-maven-plugin**: Se encarga de medir la cobertura de código de tus pruebas. Se configura para generar un informe HTML después de que se ejecutan las pruebas, lo que te permite ver qué partes de tu código están cubiertas por los tests.


- **spring-boot-maven-plugin**: Empaqueta el proyecto en un archivo JAR o WAR ejecutable, facilitando su despliegue y ejecución.
