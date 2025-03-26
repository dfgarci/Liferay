Instalación y Configuración en Windows

Para instalar Liferay de manera local en Windows, sigue estos pasos:

1. Descargar Liferay

Visita la página oficial de Liferay y elige la versión Community Edition (CE) o DXP. Descarga el paquete con Tomcat, que es la opción más sencilla para comenzar.

2. Extraer el archivo descargado

Descomprime el archivo en una ubicación de tu preferencia, por ejemplo:

C:\Liferay\

3. Configurar Java

Liferay requiere Java Development Kit (JDK) 8 o superior. Para verificar si tienes Java instalado, abre una terminal y ejecuta:

java -version

Si no tienes Java, descárgalo desde Oracle o usa OpenJDK.

Luego, configura la variable de entorno JAVA_HOME:

Ve a Panel de control > Sistema > Configuración avanzada del sistema.

En Variables de entorno, crea una nueva variable llamada JAVA_HOME y apunta a la carpeta donde instalaste Java.

4. Configurar la base de datos

Liferay puede trabajar con bases de datos como MySQL, PostgreSQL y SQL Server. Si no quieres usar la base de datos embebida, instala MySQL y crea una base de datos para Liferay:

CREATE DATABASE liferay DEFAULT CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
CREATE USER 'liferay'@'localhost' IDENTIFIED BY 'password';
GRANT ALL PRIVILEGES ON liferay.* TO 'liferay'@'localhost';
FLUSH PRIVILEGES;

Luego, en C:\Liferay\portal-ext.properties, configura:

jdbc.default.driverClassName=com.mysql.cj.jdbc.Driver
jdbc.default.url=jdbc:mysql://localhost:3306/liferay?useUnicode=true&characterEncoding=UTF-8&useSSL=false&serverTimezone=UTC
jdbc.default.username=liferay
jdbc.default.password=password

5. Ejecutar Liferay en Windows

Dirígete a la carpeta tomcat/bin dentro de la instalación de Liferay y ejecuta:

startup.bat

Si ves un error de permisos, prueba ejecutarlo como administrador.

6. Acceder a Liferay

Abre tu navegador y visita:

http://localhost:8080

Sigue los pasos del asistente de configuración para completar la instalación.
