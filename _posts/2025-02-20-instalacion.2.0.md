---
layout: default
title: "Instalación y configuración inicial"
date: 2025-03-21
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

Para instalar Liferay de manera local en Windows, sigue estos pasos junto con la guía de este video:

https://www.youtube.com/watch?v=hkupt1WJXCo&ab_channel=OpenWebinars

### **1. Descargar Liferay**

- Visita la [página oficial de Liferay](https://www.liferay.com/downloads) y elige la versión Community Edition (CE) o DXP.
- O visite su página en Github para revisar versiones anteriores:
-   (https://github.com/liferay/liferay-portal/releases)
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

### **5. Ejecutar Liferay en Eclipse**

Crea un **Worckspace** en la carpeta 

```plaintext
C:\Liferay\nombre-del-workspace
```

Abre Eclipse con el **Worckspace** establecido 

![image](https://github.com/user-attachments/assets/5d8a7140-1545-4e1f-8156-4ab85443c66b)

Ahora seleciona **New Liferay Workspace**

![image](https://github.com/user-attachments/assets/bda8591a-9095-4a66-8302-e98f62e391dd)

Luego de nombrar el nuevo entorno selecciona abrir con perspectiva de entorno y tendras una vista asi:

![image](https://github.com/user-attachments/assets/d48ba29a-34a2-4efa-bd45-44d0bdfa58fa)

Luego agrega un nuevo servidor y selecciona tipo de servidor **Liferay 7.x** y configura el **Directorio del Bundle de Liferay Portal** y el **JRE runtime**

![image](https://github.com/user-attachments/assets/c6c9c0e5-93b2-4855-b6c9-61418c7bd149)

![image](https://github.com/user-attachments/assets/284864db-25d5-4da4-94b5-80c56c327151)

**Nota: la version de JAVA instalada y configurada en las variables de entorno deben ser las mismas del JRE runtime del servidor y del compilador de Eclipse**

Una vez configurado el servidor **Ejecutar**, el resultado sera:

![image](https://github.com/user-attachments/assets/97ea223c-e769-4a24-8ca0-c6c6c1d77f64)

Abre tu navegador y visita:

```plaintext
http://localhost:8080
```

Sigue los pasos del asistente de configuración para completar la instalación.

---

Si tienes dudas o sugerencias, ¡déjalas en los comentarios! 🚀

