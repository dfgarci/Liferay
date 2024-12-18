---
layout: default
title: "Instalación y configuración inicial"
date: 2024-12-16
categories: [liferay, instalación, tutorial, Eclipse]
---

# Instalación y configuración inicial

En esta guía aprenderás cómo instalar Liferay y configurar tu entorno de desarrollo de forma local. Al finalizar, tendrás un entorno funcional para empezar a crear tus proyectos.

---

## 1. Descarga de Liferay y herramientas necesarias

### Liferay Portal
1. Ve a la página oficial de [descargas de Liferay](https://www.liferay.com/es/downloads-community).
2. Selecciona la versión **Community Edition** más reciente.
3. Descarga el paquete `Tomcat Bundle` para una instalación rápida.

### JDK 8
1. Asegúrate de tener **Java JDK 8** instalado. 
   - Para verificar: abre la terminal y ejecuta:
     ```bash
     java -version
     ```
   - Si no lo tienes instalado, descárgalo desde [Oracle JDK](https://www.oracle.com/es/java/technologies/javase/javase8-archive-downloads.html) o usa una alternativa como OpenJDK.

### Eclipse IDE
1. Descarga e instala [Eclipse IDE para desarrolladores Java EE](https://eclipseide.org/).
2. Instala el plugin de Liferay:
   - Ve a `Help > Eclipse Marketplace`.
   - Busca `Liferay IDE` e instálalo.

---

## 2. Configuración del servidor

### Configuración de Liferay
1. Descomprime el paquete descargado en una ubicación de tu preferencia.
2. Abre la carpeta descomprimida y localiza el archivo `startup.bat` (Windows) o `startup.sh` (Mac/Linux).
3. Ejecuta el archivo para iniciar el servidor. Una vez iniciado, accede a:

   ___https://localhost:8080___

5. Sigue las instrucciones en pantalla para crear un usuario administrador.

---

## 3. Configuración en Eclipse

1. Abre Eclipse y crea un nuevo **Liferay Workspace**:
- Ve a `File > New > Liferay Workspace Project`.
- Elige un nombre y configura la versión de Liferay que usarás.

2. Configura el servidor de Liferay:
- Ve a `Window > Show View > Servers`.
- Haz clic derecho en la vista y selecciona `New > Server`.
- Busca y selecciona **Liferay Server**.
- Vincula la ubicación del bundle descargado anteriormente.

---

## 4. Verificación de la instalación

1. En Eclipse, asegúrate de que el servidor esté en estado **Running**.
2. Abre tu navegador y verifica que Liferay cargue correctamente:

   ___https://localhost:8080___
   
4. Crea un sitio de prueba para confirmar que todo esté funcionando.

---

¡Listo! Ahora tienes tu entorno inicial configurado y puedes empezar a desarrollar en Liferay.


