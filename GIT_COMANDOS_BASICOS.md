\# 🚀 Git - Comandos Básicos - Guía Rápida



\## 📋 Comandos Esenciales Diarios



\### ✅ Ver estado del repositorio

```bash

git status

```

\*\*Cuándo usar:\*\* Antes de hacer commit, para ver qué archivos cambiaron.



---



\### ➕ Agregar archivos al staging

```bash

\# Agregar un archivo específico

git add nombre\_archivo.md



\# Agregar todos los archivos modificados

git add .



\# Agregar una carpeta completa

git add nombre\_carpeta/

```

\*\*Cuándo usar:\*\* Después de crear o modificar archivos, antes de commit.



---



\### 💾 Hacer commit (guardar cambios)

```bash

git commit -m "Descripción clara del cambio"

```

\*\*Ejemplos de buenos mensajes:\*\*

\- `"Agregar template de matrices TCM"`

\- `"Corregir error en precondiciones"`

\- `"Actualizar README con instrucciones"`



---



\### 🚀 Subir cambios a GitHub

```bash

git push origin master

```

\*\*Cuándo usar:\*\* Después de hacer commit(s), para subir a GitHub.



---



\### 🔄 Actualizar desde GitHub (traer cambios)

```bash

git pull origin master

```

\*\*Cuándo usar:\*\* Si trabajas desde otra computadora o alguien más hizo cambios.



---



\## 📂 Comandos de Información



\### 📜 Ver historial de commits

```bash

\# Ver últimos 5 commits

git log --oneline -5



\# Ver todos los commits

git log --oneline



\# Ver detalles completos

git log

```



---



\### 📁 Ver archivos en el repositorio

```bash

git ls-files

```



---



\### 🔍 Ver diferencias

```bash

\# Ver qué cambió en archivos no commiteados

git diff



\# Ver cambios en un archivo específico

git diff nombre\_archivo.md

```



---



\## ⚙️ Configuración Inicial (solo una vez)



\### 👤 Configurar identidad

```bash

git config user.name "Gpereira2024"

git config user.email "gpereira@T-IDSOLUTIONS.COM"

```



---



\### 🔗 Vincular con GitHub

```bash

git remote add origin https://github.com/Gpereira2024/nombre-repo.git

```



---



\### ✅ Verificar configuración

```bash

\# Ver toda la configuración

git config --list



\# Ver solo usuario y email

git config user.name

git config user.email



\# Ver repositorio remoto

git remote -v

```



---



\## 🗂️ Comandos de Gestión de Archivos



\### ➕ Agregar nueva carpeta

```bash

\# Mover carpeta al repo

Move-Item "C:\\ruta\\carpeta" "C:\\QA\_Claude\\carpeta"



\# Agregar al Git

cd C:\\QA\_Claude

git add carpeta/

git commit -m "Agregar carpeta con archivos del proyecto"

git push origin master

```



---



\### 🗑️ Eliminar archivo del repositorio

```bash

\# Eliminar archivo

git rm nombre\_archivo.md



\# Commit del cambio

git commit -m "Eliminar archivo obsoleto"



\# Subir

git push origin master

```



---



\### 📝 Renombrar archivo

```bash

\# Renombrar

git mv viejo\_nombre.md nuevo\_nombre.md



\# Commit

git commit -m "Renombrar archivo"



\# Subir

git push origin master

```



---



\## 🔧 Comandos de Ramas (Branches)



\### 🌿 Ver ramas

```bash

\# Ver rama actual

git branch



\# Ver todas las ramas (locales y remotas)

git branch -a

```



---



\### ➕ Crear y cambiar de rama

```bash

\# Crear nueva rama

git branch nombre-rama



\# Cambiar a la rama

git checkout nombre-rama



\# Crear y cambiar en un solo comando

git checkout -b nombre-rama

```



---



\### 🔄 Cambiar nombre de rama

```bash

\# Renombrar rama actual a "main"

git branch -M main

```



---



\## 🚨 Comandos de Emergencia



\### ↩️ Deshacer cambios NO commiteados

```bash

\# Deshacer cambios en un archivo

git checkout -- nombre\_archivo.md



\# Deshacer TODOS los cambios

git reset --hard

```

\*\*⚠️ CUIDADO:\*\* Esto elimina cambios permanentemente.



---



\### 🔙 Quitar archivos del staging (antes de commit)

```bash

\# Quitar un archivo del staging

git reset nombre\_archivo.md



\# Quitar todos los archivos del staging

git reset

```



---



\### ⏮️ Deshacer último commit (mantener cambios)

```bash

git reset --soft HEAD~1

```

\*\*Útil si:\*\* Olvidaste agregar algo al commit.



---



\### ⏮️ Deshacer último commit (eliminar cambios)

```bash

git reset --hard HEAD~1

```

\*\*⚠️ CUIDADO:\*\* Elimina el commit Y los cambios.



---



\## 🔄 Flujo de Trabajo Típico



```bash

\# 1. Ver qué cambió

git status



\# 2. Agregar archivos

git add archivo.md

\# o

git add .



\# 3. Ver qué se va a commitear

git status



\# 4. Hacer commit

git commit -m "Descripción del cambio"



\# 5. Subir a GitHub

git push origin master



\# 6. Verificar en navegador

\# https://github.com/Gpereira2024/QA\_Claude

```



---



\## 🎯 Casos de Uso Comunes



\### ✅ Agregar nuevo archivo

```bash

\# Crear archivo (PowerShell, VS Code, etc.)

\# Luego:

git add nuevo\_archivo.md

git commit -m "Agregar nuevo archivo"

git push origin master

```



---



\### ✅ Modificar archivo existente

```bash

\# Editar archivo

\# Luego:

git add archivo\_modificado.md

git commit -m "Actualizar contenido del archivo"

git push origin master

```



---



\### ✅ Agregar múltiples archivos

```bash

git add archivo1.md archivo2.md archivo3.md

git commit -m "Agregar varios archivos relacionados"

git push origin master

```



---



\### ✅ Subir carpeta completa

```bash

git add nombre\_carpeta/

git commit -m "Agregar carpeta con archivos del proyecto"

git push origin master

```



---



\## 🛠️ Solución de Problemas



\### ❌ Error: "Permission denied"

```bash

\# Verificar credenciales guardadas

git credential-manager github logout nombre-cuenta



\# Intentar push de nuevo

git push origin master

\# Te pedirá credenciales nuevas

```



---



\### ❌ Error: "Nothing to commit"

\*\*Causa:\*\* No hay cambios nuevos.

\*\*Solución:\*\* Verifica con `git status` si realmente modificaste archivos.



---



\### ❌ Error: "Please commit or stash them"

```bash

\# Opción 1: Guardar cambios

git add .

git commit -m "Guardar cambios antes de pull"



\# Opción 2: Descartar cambios

git reset --hard

```



---



\### ❌ Conflictos al hacer pull

```bash

\# Ver archivos en conflicto

git status



\# Editar archivos manualmente para resolver

\# Buscar marcas: <<<<<<< ======= >>>>>>>



\# Después de resolver:

git add archivo\_resuelto.md

git commit -m "Resolver conflicto"

git push origin master

```



---



\## 📚 Recursos Adicionales



\- \*\*Documentación oficial:\*\* https://git-scm.com/doc

\- \*\*Tu repositorio:\*\* https://github.com/Gpereira2024/QA\_Claude

\- \*\*Configurar tokens:\*\* https://github.com/settings/tokens



---



\## 💡 Tips Importantes



1\. \*\*Siempre hacer `git status` antes de commit\*\* para ver qué cambió

2\. \*\*Commits frecuentes con mensajes claros\*\* mejor que uno grande

3\. \*\*Pull antes de empezar a trabajar\*\* si usas múltiples computadoras

4\. \*\*Push al final del día\*\* para respaldar tu trabajo

5\. \*\*No commitear archivos sensibles\*\* (contraseñas, tokens, etc.)



---



\## 🔐 Archivo .gitignore (Ignorar archivos)



Crear archivo `.gitignore` en la raíz del repo:



```

\# Ignorar archivos de sistema

.DS\_Store

Thumbs.db



\# Ignorar archivos temporales

\*.tmp

\*.log

~$\*



\# Ignorar carpetas

node\_modules/

.vscode/

\_\_pycache\_\_/



\# Ignorar archivos sensibles

.env

secrets.txt

\*.key

```



---



\*\*Versión:\*\* 1.0  

\*\*Última actualización:\*\* 2026-02-04  

\*\*Usuario:\*\* Gpereira2024  

\*\*Repositorio:\*\* QA\_Claude



---



\## 🚀 Inicio Rápido



```bash

\# Navegar al repositorio

cd C:\\QA\_Claude



\# Ver estado

git status



\# Agregar cambios

git add .



\# Commit

git commit -m "Descripción"



\# Subir

git push origin master

```



\*\*¡Listo para trabajar!\*\* 🎉

