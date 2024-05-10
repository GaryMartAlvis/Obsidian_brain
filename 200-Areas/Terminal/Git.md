### Lista de comandos

```bash
git init # Inicia un nuevo repositorio de Git
git status # Agrega cambios al área de preparación
git add <archivo_o_directorio> # Agrega cambios al área de preparación
git commit -m "Mensaje del commit" # Registra los cambios en el repositorio
git log --all --oneline # Muestra el historial de commits visualizados en una sola línea
git clone <url_del_repositorio> # Clona un repositorio existente en un nuevo directorio
git pull origin # Obtiene cambios desde un repositorio remoto y los fusiona en el repositorio local
git push origin # Sube los cambios locales a un repositorio remoto
git branch # Lista las ramas en el repositorio
git checkout <nombre_de_rama> # Cambia de rama o restaura archivos
git merge <rama_a_fusionar> # Fusiona una rama en la rama actual
git remote -v # Muestra los repositorios remotos configurados
git fetch origin # Obtiene los cambios del repositorio remoto sin fusionarlos
git diff # Muestra las diferencias entre cambios en el área de preparación y el directorio de trabajo
git reset --hard # Deshace cambios locales
git tag -a <nombre_etiq> -m "Mensaje Etiq" # Crea, lista o borra etiquetas
```

### Pushear archivos locales a un repositorio nuevo en GitHub

```bash
git init
git add .
git commit -m 'Repository initialization'
git branch -M main
git remote add origin <url_repository_github>
git push -u origin main
```

### Creación y conexión de repositorio con GitHub

```bash
# Comando sujeridos al crear un repositorio en GitHub
# Or create a new repository on the command line
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin <URL-Repository>
git push -u origin main

# Or push an existing repository from the command line
git remote add origin <URL-Repository>
git branch -M main
git push -u origin main
```

### Configuración global de Git

```bash
git config --global --list

# Abrir editor para cambiar las configuraciones globales 
> git config --global --edit

# Ejemplo de configuración
    	[user]
		    name = GaryMartAlvis
		    email = gary.martinez.alvis@gmail.com

    # Abrir archivo de configuración con notepad
    > notepad ~/.gitconfig

    # Configurar para abrir con un editor especifico
    > git config --global core.editor "notepad"</>
```

<details>
<summary>Como hacer un Pull request</summary>

Pasos para realizar un pull request

Step 1: Hacer Fork del repositorio original**

Hacer un fork en GitHub significa crear una copia personal de un repositorio ajeno en tu propia cuenta de GitHub. Esto te permite trabajar en el proyecto sin afectar el repositorio original. La copia (fork) está vinculada al repositorio original, lo que facilita la colaboración y la contribución a proyectos de código abierto o a proyectos de otras personas.

- Ingresa a GitHub
- Encuentra el repositorio
- Abre el repositorio
- Hacer Fork:En la esquina superior derecha de la página del repositorio, encontrarás el botón "Fork". Haz clic en él.
- Elige la cuenta: Selecciona tu cuenta como destino para el fork. Esto creará una copia del repositorio en tu propia cuenta.
- Espera a que se complete: GitHub creará una copia del repositorio en tu cuenta. Esto puede tardar un momento, dependiendo del tamaño del repositorio.

Step 2: Clona el repositorio en tu equipo

>>> git clone [URL_repositorio_original] 

Step 3: Crea un rama para los trabajar en ella en los cambios del**

>>> git checkout -b nombre-de-tu-rama

Step 4: Realizar cambios locales

Realiza los cambios que desees en tu rama local. Puedes agregar, modificar o eliminar archivos según sea necesario.

Step 5: Hacer commit de los cambios

>>> git add .
>>> git commit -m "Mensaje descriptivo de tus cambios"

Step 6: Subir cambios a tu repositorio Forked

>>> git push origin nombre-de-tu-rama

Step 7: Crear el pull request

- Ve a tu repositorio forked en GitHub.
- Cambia a la rama que acabas de crear.
- Haz clic en el botón "New Pull Request".

Step 8: Completar la Información del Pull Request**

- Asegúrate de que la rama base (base branch) sea la rama correcta del repositorio original.
- Asegúrate de que la rama de comparación (compare branch) sea tu rama con los cambios.
- Proporciona un título y una descripción descriptiva para explicar tus cambios.

Step 9: Crear el Pull Request

- Haz clic en el botón "Create Pull Request".
- Añade comentarios adicionales si es necesario.

Step 10: Espera la revisión y fusión**

Los propietarios del repositorio original revisarán tus cambios. Puede haber comentarios, preguntas o solicitudes de ajustes. Una vez que tus cambios sean aceptados y fusionados, tu Pull Request estará cerrado.

</details>