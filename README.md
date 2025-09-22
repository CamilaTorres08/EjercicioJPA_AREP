## Ejercicio JPA - Spring Boot (Taller 5)

Pequeño ejemplo de persistencia con Spring Data JPA usando una base en memoria H2. Al iniciar la aplicación se insertan algunos `Customer` y se ejecutan consultas básicas, registrando los resultados en el log.

### Tecnologías
- **Spring Boot 3** (starter data JPA)
- **H2** (runtime, en memoria)
- **Java 17**
- Maven Wrapper

### Dominio
- `Customer` (Entidad JPA): campos `id`, `firstName`, `lastName`.
- `CustomerRepository` (Spring Data `CrudRepository`):
  - `findByLastName(String lastName)`
  - `findById(long id)`

Al arrancar, `Taller5Application` (via `CommandLineRunner`) guarda varios clientes y muestra por log:
- Todos los clientes
- Cliente con `id = 1`
- Clientes con `lastName = "Bauer"`

### Requisitos
- Java 17 instalado y en `PATH`.

### Cómo ejecutar (Windows PowerShell)
- Compilar y ejecutar:
  ```bash
  .\mvnw.cmd spring-boot:run
  ```
- Ejecutar pruebas:
  ```bash
  .\mvnw.cmd test
  ```

La aplicación no expone endpoints HTTP; el comportamiento se observa en la consola por los logs al iniciar.

### Estructura relevante
- `src/main/java/eci/edu/arep/taller5/Model/Customer.java`
- `src/main/java/eci/edu/arep/taller5/Repository/CustomerRepository.java`
- `src/main/java/eci/edu/arep/taller5/Taller5Application.java`
- `src/main/resources/application.properties`

### Evidencia AWS-CLI
En el archivo `informeAWS` se encuentra la evidencia del ejercicio **AWS-CLI Primer Workshop** para crear una instancia EC2 por medio de AWS-CLI.

## Autor
Andrea Camila Torres González


