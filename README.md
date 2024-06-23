# allura-challenge-literalura
Tercer desafío de Java Backend de Allura Latam - Catálogo de Libros
 

## 🎯 Funcionalidades implementadas
- Menú de opciones listando las operaciones más recurrentes de consulta de libros y autores:
  -> Buscar libros por título
  -> Listar libros registrados
  -> Listar autores registrados
  -> Listar autores vivos en un determinado año
  -> Listar libros por idioma (previa salida mostrando los idiomas disponibles según los libros ya registrados en la DB)
- Chequeo de entrada de datos erróneos
- Persistencia permanente de datos consultados a la API en Postgres DB
 
## 🔎 Requisitos
JAVA 17
Maven 3.3.2
Git

## 🔩 Configuración
Para poder conectar con una base de datos local se deben configurar los siguientes parámetros en el archivo src/main/resources/application.properties.

spring.datasource.url=jdbc:postgresql://{tu_host}:5455/{tu_base_de_datos}
spring.datasource.username= {tu_nombre_usuario} 
spring.datasource.password= {tu_password_usuario}
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
spring.jpa.database-platform=org.hibernate.dialect.MySQLDialect

🤘 Si tienes DOCKER puede rápidamente crear tu container de Postgres y levantarlo en local, pull de la imagen incluido, con la siguiente linea de comando en tu CMD o Bash 
(reemplazando los parámetros en concordancia con lo detallado en el application.properties, obviamente si colocar las llaves {}, sólo las variables, siendo el tu_host el valor 'localhost')
docker run --name {NOMBRE_DE_TU_CONTENEDOR} -p 5455:5432 -e POSTGRES_USER={tu_nombre_usuario} -e POSTGRES_PASSWORD={tu_password_usuario} -e POSTGRES_DB={tu_base_de_datos} -d postgres
 
