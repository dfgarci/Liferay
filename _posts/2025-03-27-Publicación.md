---
layout: default
title: "Publicación y Administración en Liferay"
date: 2025-03-27
categories: [liferay, publicación, administración, tutorial, Eclipse]
---

# Publicación y Administración en Liferay

## **1. Publicar un Portlet en Liferay**

Después de crear un portlet en Liferay, es necesario desplegarlo y administrarlo dentro del portal. Sigue estos pasos para asegurarte de que tu portlet esté correctamente publicado.

### **1.1 Desplegar el Portlet en el Servidor**

1. Abre **Eclipse** y asegúrate de que tu servidor de Liferay está en ejecución.
2. En el **Explorador de proyectos**, haz clic derecho sobre el proyecto del portlet.
3. Selecciona **Liferay > Deploy**.
4. Espera a que finalice la compilación y confirmación en la consola.

### **1.2 Agregar el Portlet a una Página**

1. Inicia sesión en Liferay como administrador.
2. Ve a **Control Panel > Site > Pages**.
3. Selecciona una página existente o crea una nueva.
4. En el menú lateral, selecciona "Widgets" y busca tu portlet.
5. Arrástralo a la página y guarda los cambios.

---

## **2. Administrar Permisos del Portlet**

Liferay permite configurar los permisos para controlar quién puede ver y modificar un portlet.

### **2.1 Configurar Permisos**

1. Ve a la página donde agregaste el portlet.
2. Haz clic en el icono de opciones del portlet y selecciona **Configuración**.
3. Ve a la pestaña **Permisos**.
4. Define qué roles pueden ver, configurar o administrar el portlet.
5. Guarda los cambios.

---

## **3. Administrar el Portlet desde el Panel de Control**

Desde el **Panel de Control**, puedes administrar portlets instalados en Liferay:

1. Ve a **Control Panel > Apps > App Manager**.
2. Busca el nombre de tu portlet en la lista.
3. Desde aquí puedes:
   - Ver información detallada del portlet.
   - Desactivar o eliminar el portlet si es necesario.

---

¡Con estos pasos, tu portlet estará correctamente publicado y administrado en Liferay! 🚀

