---
layout: default
title: "Instalación y configuración inicial"
date: 2024-12-16
categories: [liferay, instalación, tutorial, Eclipse]
---

# Introducción a Liferay: Primeros Pasos para Desarrolladores

Liferay puede parecer abrumador al principio, pero una vez que entiendes su estructura y cómo manejar los portlets e integrar APIs, se vuelve una herramienta poderosa. En este blog, quiero compartir mi experiencia aprendiendo Liferay, con explicaciones sencillas y ejemplos prácticos.

## ¿Qué es Liferay y por qué usarlo?

Liferay es un **portal empresarial** basado en Java que permite crear sitios web dinámicos con funcionalidades listas para usar, como gestión de usuarios, contenido y permisos. Se utiliza ampliamente para intranets, portales corporativos y sistemas de gestión de información.

### Características clave:
- Basado en **Java y OSGi**.
- Modularidad mediante **portlets**.
- Integración con bases de datos y APIs REST/SOAP.
- Extensibilidad con temas, hooks y servicios personalizados.

## Instalación y Configuración en Windows

Para instalar Liferay de manera local en Windows, sigue estos pasos:

### **1. Descargar Liferay**

- Visita la [página oficial de Liferay](https://www.liferay.com/downloads) y elige la versión Community Edition (CE) o DXP.
- Descarga la opción con **Tomcat**, que es la más sencilla para comenzar.

### **2. Extraer el archivo descargado**

Descomprime el archivo en una ubicación de tu preferencia, por ejemplo:

```plaintext
C:\Liferay\
```

### **3. Configurar Java**

Liferay requiere **Java Development Kit (JDK) 8 o superior**. Para verificar si tienes Java instalado, abre una terminal y ejecuta:

```sh
java -version
```

Si no tienes Java, descárgalo desde [Oracle](https://www.oracle.com/java/technologies/javase-downloads.html) o usa OpenJDK.

Luego, configura la variable de entorno `JAVA_HOME`:

1. Ve a *Panel de control > Sistema > Configuración avanzada del sistema*.
2. En *Variables de entorno*, crea una nueva variable llamada `JAVA_HOME` y apunta a la carpeta donde instalaste Java.

### **4. Configurar la base de datos (Opcional)**

Liferay puede trabajar con bases de datos como MySQL, PostgreSQL y SQL Server. Si no quieres usar la base de datos embebida, instala MySQL y crea una base de datos para Liferay con los siguientes comandos:

```sql
CREATE DATABASE liferay DEFAULT CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
CREATE USER 'liferay'@'localhost' IDENTIFIED BY 'password';
GRANT ALL PRIVILEGES ON liferay.* TO 'liferay'@'localhost';
FLUSH PRIVILEGES;
```

Luego, en `C:\Liferay\portal-ext.properties`, configura la conexión con la base de datos:

```properties
jdbc.default.driverClassName=com.mysql.cj.jdbc.Driver
jdbc.default.url=jdbc:mysql://localhost:3306/liferay?useUnicode=true&characterEncoding=UTF-8&useSSL=false&serverTimezone=UTC
jdbc.default.username=liferay
jdbc.default.password=password
```

### **5. Ejecutar Liferay en Windows**

Dirígete a la carpeta `tomcat/bin` dentro de la instalación de Liferay y ejecuta:

```sh
startup.bat
```

Si ves un error de permisos, prueba ejecutarlo como administrador.

### **6. Acceder a Liferay**

Abre tu navegador y visita:

```plaintext
http://localhost:8080
```

Sigue los pasos del asistente de configuración para completar la instalación.

---

Si tienes dudas o sugerencias, ¡déjalas en los comentarios! 🚀


