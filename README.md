# basicogit

Este repositorio contiene los comandos básicos de Git y GitHub como base para la materia de **Programación Orientada a Objetos**.

---

## ¿Qué es Git?

Git es un sistema de control de versiones distribuido que permite registrar los cambios en el código fuente a lo largo del tiempo.

---

## Configuración inicial

```bash
# Configurar nombre de usuario
git config --global user.name "Tu Nombre"

# Configurar correo electrónico
git config --global user.email "tu@correo.com"

# Ver configuración actual
git config --list
```

---

## Comandos básicos

### Inicializar un repositorio

```bash
# Crear un nuevo repositorio local
git init

# Clonar un repositorio existente de GitHub
git clone https://github.com/usuario/repositorio.git
```

### Estado y seguimiento de archivos

```bash
# Ver el estado del repositorio
git status

# Agregar un archivo al área de preparación (staging)
git add nombre_archivo.txt

# Agregar todos los archivos modificados
git add .

# Ver diferencias entre el directorio de trabajo y el staging
git diff
```

### Confirmar cambios (commits)

```bash
# Crear un commit con un mensaje descriptivo
git commit -m "Mensaje descriptivo del cambio"

# Agregar y confirmar en un solo paso (solo archivos ya rastreados)
git commit -am "Mensaje del commit"

# Ver el historial de commits
git log

# Ver el historial de forma resumida
git log --oneline
```

### Ramas (branches)

```bash
# Ver todas las ramas
git branch

# Crear una nueva rama
git branch nombre-rama

# Cambiar a una rama existente
git checkout nombre-rama

# Crear y cambiar a una nueva rama en un solo paso
git checkout -b nueva-rama

# Fusionar una rama con la rama actual
git merge nombre-rama

# Eliminar una rama
git branch -d nombre-rama
```

### Trabajo con repositorios remotos (GitHub)

```bash
# Ver los repositorios remotos configurados
git remote -v

# Agregar un repositorio remoto
git remote add origin https://github.com/usuario/repositorio.git

# Enviar cambios al repositorio remoto
git push origin main

# Descargar y fusionar cambios del repositorio remoto
git pull origin main

# Descargar cambios sin fusionar
git fetch origin
```

### Deshacer cambios

```bash
# Descartar cambios en un archivo (antes del staging)
git checkout -- nombre_archivo.txt

# Quitar un archivo del staging
git reset HEAD nombre_archivo.txt

# Revertir el último commit (mantiene los cambios en el directorio)
git reset --soft HEAD~1

# Revertir el último commit (descarta los cambios)
git reset --hard HEAD~1
```

---

## Flujo de trabajo típico

1. `git clone` — Clonar el repositorio.
2. `git checkout -b` — Crear una rama para el nuevo trabajo.
3. Editar archivos.
4. `git add .` — Agregar cambios al staging.
5. `git commit -m "..."` — Confirmar los cambios.
6. `git push origin nombre-rama` — Enviar la rama a GitHub.
7. Crear un **Pull Request** en GitHub para integrar los cambios.

---

## Recursos adicionales

- [Documentación oficial de Git](https://git-scm.com/doc)
- [GitHub Docs](https://docs.github.com/)
- [Pro Git (libro gratuito)](https://git-scm.com/book/es/v2)
