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
   - Si no lo tienes instalado, descárgalo desde [Oracle JDK](https://www.oracle.com/java/technologies/javase/javase-jdk8-downloads.html) o usa una alternativa como OpenJDK.

### Eclipse IDE
1. Descarga e instala [Eclipse IDE para desarrolladores Java EE](https://www.eclipse.org/downloads/).
2. Instala el plugin de Liferay:
   - Ve a `Help > Eclipse Marketplace`.
   - Busca `Liferay IDE` e instálalo.

---

## 2. Configuración del servidor

### Configuración de Liferay
1. Descomprime el paquete descargado en una ubicación de tu preferencia.
2. Abre la carpeta descomprimida y localiza el archivo `startup.bat` (Windows) o `startup.sh` (Mac/Linux).
3. Ejecuta el archivo para iniciar el servidor. Una vez iniciado, accede a:
