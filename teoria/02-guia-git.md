# Machete de Git/GitHub 🐙

Guía rápida de los comandos que vamos a usar en clase. No hace falta memorizarlos todos: con `clone`, `status`, `add`, `commit`, `push` y `pull` ya pueden trabajar tranquilos.

---

## 🧠 Primero, ¿qué es cada cosa?

- **Git**: el programa que corre en tu computadora y lleva el "historial" de cambios de tu proyecto.
- **GitHub**: una página web donde se guarda una copia de ese proyecto (el "repo") para que todos puedan verla y trabajar en conjunto.
- **Repositorio (repo)**: la carpeta de tu proyecto, pero con todo el historial de cambios guardado por Git.

Pensalo como un **Google Docs del código**: cada `commit` es como guardar una versión con un nombre, y `push`/`pull` son subir o bajar esos cambios.

---

## 1️⃣ Clonar un repositorio (la primera vez)

Descarga una copia del repo a tu computadora.

```bash
git clone https://github.com/usuario/nombre-del-repo.git
```

Esto crea una carpeta nueva con todo el contenido del repositorio.

---

## 2️⃣ Ver el estado de tus cambios

```bash
git status
```

Te muestra:
- Qué archivos modificaste.
- Qué archivos son nuevos (no están siendo rastreados todavía).
- Qué archivos ya están listos para subir (en "staging").

> 🔍 **Tip**: usen `git status` todo el tiempo. Nunca está de más chequear antes de hacer un commit.

---

## 3️⃣ Agregar cambios (staging)

Antes de "guardar" una versión, hay que decirle a Git **qué** archivos queremos incluir.

```bash
git add nombre_archivo.py     # Agregar un archivo puntual
git add .                     # Agregar TODOS los archivos modificados
```

---

## 4️⃣ Hacer un commit (guardar la versión)

```bash
git commit -m "Mensaje describiendo qué cambié"
```

El mensaje es importante: tiene que explicar **qué se hizo**, no decir cosas como "cambios" o "arreglos".

✅ Buen mensaje: `git commit -m "Agrego clase Perro con metodo ladrar"`
❌ Mal mensaje: `git commit -m "asd"`

---

## 5️⃣ Subir los cambios a GitHub

```bash
git push
```

Esto sube tus commits locales al repositorio en GitHub, para que los demás los vean.

---

## 6️⃣ Bajar los cambios de los demás

```bash
git pull
```

Trae los cambios que otros subieron a GitHub y los mezcla con tu copia local. Conviene hacer `pull` antes de empezar a trabajar, para no pisarse con cambios de otros.

---

## 🔁 El flujo típico de trabajo

```bash
git pull                          # 1. Traigo los últimos cambios
# ... edito mis archivos ...
git status                        # 2. Veo qué cambié
git add .                         # 3. Marco los cambios
git commit -m "Mensaje claro"     # 4. Guardo la versión
git push                          # 5. Subo a GitHub
```

---

## 🆘 Comandos útiles extra

| Comando | ¿Para qué sirve? |
|---|---|
| `git log` | Ver el historial de commits |
| `git diff` | Ver qué líneas exactas cambiaron |
| `git branch` | Ver en qué rama estoy |
| `git checkout -b nombre-rama` | Crear y moverme a una rama nueva |

---

## ⚠️ Errores comunes

- **"fatal: not a git repository"** → Te falta hacer `cd` a la carpeta del repo, o todavía no clonaste nada.
- **"Updates were rejected"** al hacer `push` → Alguien subió cambios antes que vos. Hacé `git pull` primero y después `push` de nuevo.
- Olvidarse el `-m "mensaje"` en el commit → Git va a abrir un editor de texto raro (vim). Para salir sin guardar: `Esc` y después escribir `:q!`.
