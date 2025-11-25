# PROYECTO FINAL GIT - ADSO

Este repositorio es el resultado del taller de introducción a Git y GitHub.

## Datos del Taller

**Objetivo del proyecto:**  Aprender a manejar el flujo de trabajo de Git (configuración, inicialización, staging, commit, ramas y push/pull) en un entorno colaborativo.

**Integrantes:**
- Nombre: Cristian Yair Gutierrez Bejarano
- Correo: gameplaycristian98@gmail.com

**Fecha:** 24 de Noviembre de 2025

---

## 💡 ¿Qué es Git? 

Git es un **sistema de control de versiones distribuido (DVCS)**, que permite a los desarrolladores rastrear de forma eficiente los cambios en el código fuente de un proyecto a lo largo del tiempo.

A diferencia de los sistemas centralizados, en Git, cada desarrollador tiene una copia completa del historial del proyecto en su máquina local.

Su diseño se centra en la velocidad, la integridad de los datos y el soporte para flujos de trabajo no lineales, lo que lo hace ideal para la colaboración en grandes equipos.

El núcleo de Git se basa en la idea de un **commit**, que es una instantánea de todo el proyecto en un momento dado, en lugar de almacenar solo las diferencias (deltas) entre versiones.

La característica de **ramas (branches)** es fundamental, permitiendo a los desarrolladores trabajar en nuevas características o correcciones de errores de forma aislada, sin afectar la versión principal del código.

El **Área de Preparación (Staging Area)** es una zona intermedia que permite a los desarrolladores agrupar cambios específicos antes de guardarlos de forma permanente en un commit.

Esto proporciona un control granular sobre qué cambios van en cada punto del historial.

Finalmente, Git está diseñado para interactuar perfectamente con repositorios remotos (como GitHub), facilitando la sincronización y la contribución entre múltiples usuarios.

---

## 🛠️ 10 Comandos de Git Explicados

1.  **`git config`**: Configura las variables que controlan el funcionamiento y el entorno de Git (e.g., nombre de usuario y correo).
2.  **`git init`**: Inicializa un repositorio de Git en la carpeta de trabajo actual.
3.  **`git status`**: Muestra el estado de los archivos: cuáles han sido modificados, cuáles están preparados para el commit y cuáles no están siendo rastreados.
4.  **`git add .`**: Agrega todos los archivos nuevos y modificados en el directorio de trabajo al Área de Preparación (staging area).
5.  **`git commit -m "msg"`**: Guarda los cambios que están en el área de preparación en el historial del repositorio local.
6.  **`git log`**: Muestra el historial de commits, incluyendo el autor, la fecha y el mensaje.
7.  **`git branch [nombre]`**: Permite listar las ramas existentes o crear una nueva rama.
8.  **`git checkout [rama]`**: Utilizado para cambiar entre ramas o para restaurar archivos.
9.  **`git pull`**: Descarga y automáticamente fusiona los cambios de la rama remota a la rama local.
10. **`git push`**: Sube los commits locales pendientes al repositorio remoto (GitHub, GitLab, etc.).

---

## 🔄 Flujo de Trabajo Recomendado (Basado en el Módulo)

El flujo de trabajo estándar aplicado en este taller incluye los siguientes pasos clave:

1.  Creación de la carpeta local y su inicialización con `git init`.
2.  Desarrollo de las nuevas características o cambios en el código.
3.  Preparación de los cambios (`git add .`) para el próximo commit.
4.  Guardado de la instantánea en el historial (`git commit -m "Descripción"`).
5.  Conexión al repositorio remoto (`git remote add origin ...`).
6.  Sincronización y subida de los cambios al servidor remoto (`git push`).

---S

## 🛑 Sección: "Problemas encontrados hoy"

* **Problema 1:** Error al configurar `user.name` debido a la existencia de múltiples valores previos, solucionado con el *flag* `--replace-all`.
* **Problema 2:** Error de tipeo (`typo`) al intentar ingresar a la carpeta con `cd` (solucionado corrigiendo el nombre de la ruta).
* **Problema 3:** Advertencia de conversión de terminación de línea (LF a CRLF) durante `git add`, que es un comportamiento normal en Git bajo Windows y no requirió corrección manual.

## 🎉 Sección: "Conclusión del día"

Hoy completé la configuración inicial de Git y comprendí el ciclo de vida de un cambio: desde la modificación de un archivo en el Directorio de Trabajo, su paso al Área de Preparación (`git add`), hasta su guardado final como un *commit*. También logre enlazar el repositorio local con un repositorio remoto en GitHub para colaborar y respaldar el trabajo.

## 📝 Reflexión Final del Taller de Git

Aquí están mis conclusiones del ejercicio completo:

### 1. Problemas Encontrados
El principal desafío técnico fue **forzar el conflicto en el Módulo 6**. Intente modificar el mismo archivo de forma diferente, pero Git resolvió automáticamente la fusión (Fast-forward) porque los cambios no se superpusieron en la misma línea, lo que impidió la práctica manual de resolución de conflictos. Otro problema menor fue recordar subir el propio archivo **`.gitignore`** al repositorio para que sus reglas se aplicaran correctamente.

### 2. ¿Qué Aprendí Hoy?
Aprendí la **diferencia crítica entre el flujo de trabajo local (`git checkout`, `git add`, `git commit`) y el flujo de trabajo remoto (Pull Requests en GitHub)**. Comprendí que las ramas de desarrollo son fundamentales para trabajar en equipo, ya que aíslan el trabajo y el `git push` sube todo el contexto, no solo los archivos.

### 3. ¿Qué fue lo más difícil?
Lo más difícil fue **entender cómo Git maneja los archivos ignorados**. Al principio, los archivos como `.env` seguían apareciendo en el `git status` hasta que entendí que mi trabajo es asegurarme de que el **`.gitignore`** esté en el *staging area* y *commit*eado antes de crear los archivos ignorados.

### 4. Conclusión del Taller
Este taller proporcionó un flujo de trabajo de desarrollo completo y realista. Demostré la capacidad de: configurar Git, manejar múltiples ramas (`feature/login`, `feature/footer`, etc.), crear solicitudes de fusión (`Pull Requests`) en GitHub, y aplicar prácticas de limpieza de código esenciales con **`.gitignore`**. El proyecto está ahora finalizado y listo para una nueva etapa de desarrollo.