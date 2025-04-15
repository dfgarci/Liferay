# 🧙‍♂️ Blades, Gradles, and JDKs, Oh My...

> *Resumen en español del artículo de David H Nebinger sobre las nuevas versiones de herramientas para desarrolladores Liferay.*

---

## 📅 Publicado hace 9 meses | 👀 6889 visitas

---

## ✨ Introducción

Liferay ha lanzado **Liferay DXP 7.4 2024 Q2** y **Liferay CE 2024 GA 120**, acompañados de una serie de actualizaciones importantes para desarrolladores:

- Blade CLI 7.0.0  
- Gradle 8.5  
- Liferay Workspace Plugin 10.1.x  
- Soporte para JDK 17 y JDK 21

A continuación, te resumimos lo más relevante sobre cada uno de estos cambios.

---

## 🛠️ Blade 7.0.0

**Blade CLI** es la herramienta principal para crear workspaces, módulos OSGi, y gestionar despliegues localmente.

- Aunque uses Eclipse o IntelliJ, Blade sigue funcionando “detrás de escena”.
- Blade 7 se adapta automáticamente a las últimas versiones de Gradle y del plugin de Workspace.
- Puedes seguir usando Blade 7 en workspaces antiguos sin problema.
- Para actualizar: `sudo blade update` (en macOS puede requerir permisos).

> ⚠️ Los plugins de los IDE usan una versión embebida de Blade, así que debes esperar a futuras actualizaciones de esos plugins para obtener Blade 7 desde allí.

---

## ⚙️ Gradle 8.5

Los nuevos workspaces creados con Blade 7 utilizarán **Gradle 8.5** por defecto.

- Reemplaza `compile` por `implementation`.
- `compileOnly` y `compileInclude` siguen siendo válidos.
- Puedes seguir usando Gradle 6 o 7 si tu entorno no lo exige.

### Cómo actualizar:
Edita `gradle/wrapper/gradle-wrapper.properties`:
```properties
distributionUrl=https\://services.gradle.org/distributions/gradle-8.5-bin.zip
