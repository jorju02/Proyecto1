
## Aqui van los apuntes de los  comandos de git

![imagen](https://www.sgcli.com/wp-content/uploads/2018/03/github.jpg)

<u>

- ### CONFIGURAR HERRAMIENTAS</u>

    - **git config --global user.name "[name]"** --> Establece el nombre que desea esté anexado a sus transacciones de commit.
    - **git config --global user.email "[email address]"** --> Establece el e-mail que desea esté anexado a sus transacciones de commit.
    - **git config --global color.ui auto** --> Habilita la útil colorización del producto de la línea de comando
<u>  

- ### CREAR REPOSITORIOS </u>

    - **git init [project-name]** --> Crea un nuevo repositorio local con el nombre especificado
    - **git clone [url]** --> Descarga un proyecto y toda su historia de versión
<u> 

 - ### EFECTUAR CAMBIOS </u>
    
    - **git status** --> Enumera todos los archivos nuevos o modificados que se deben confirmar
    - **git diff** --> Muestra las diferencias de archivos que no se han enviado aún al área de espera
    - **git add [file]** -->Toma una instantánea del archivo para preparar la versión
    - **git diff --staged** --> Muestra las diferencias del archivo entre el área de espera y la última versión del archivo
    - **git reset [file]** --> Mueve el archivo del área de espera, pero preserva su contenido
    - **git commit -m "[descriptive message]"** --> Registra las instantáneas del archivo permanentemente en el historial de versión
<u>

- ### CAMBIOS GRUPALES</u>

    - **git branch** --> Enumera todas las ramas en el repositorio actual
    - **git branch [branch-name]** --> Crea una nueva rama
    - **git checkout [branch-name]** --> Cambia a la rama especiﬁcada y actualiza el directorio activo
    - **git merge [branch]** --> Combina el historial de la rama especiﬁcada con la rama actual
    - **git branch -d [branch-name]** --> Borra la rama especiﬁcada

   <u> 

- ### NOMBRES DEL ARCHIVO DE REFACTORIZACIÓN </u>

    - **git rm [file]** --> Borra el archivo del directorio activo y pone en el área de espera el archivo borrado
    - **git rm --cached [file]** --> Retira el archivo del control de versiones, pero preserva el archivo a nivel local

    - **git mv [file-original] [file-renamed]** --> Cambia el nombre del archivo y lo prepara para commit
    <u>

- ### REPASAR HISTORIAL </u>
    - **git log** --> Enumera el historial de la versión para la rama actual
    - **git log --follow [file]** --> Enumera el historial de versión para el archivo, incluidos los cambios de nombre
    - **git diff [first-branch]...[second-branch]** --> Muestra las diferencias de contenido entre dos ramas
    - **git show [commit]** --> Produce metadatos y cambios de contenido del commit especiﬁcado
    <u>

- ### SUPRIMIR TRACKING</u>
    - **.log build/ temp-** --> Un archivo de texto llamado .gitignore  suprime la creación accidental de versiones de archivos y rutas que concuerdan con los patrones especiﬁcados
    - **git ls-files --other --ignored --exclude-standard** --> Enumera todos los archivos ignorados en este proyect
    <u>

- ### REHACER COMMITS</u>
    - **git reset [commit]** --> Deshace todos los commits después de [commit], preservando los cambios localmente  
    - **git reset --hard [commit]** --> Desecha todo el historial y regresa al commit especiﬁcado

    <u>

- ### GUARDAR FRAGMENTOS</u>
    - **git stash** -->Almacena temporalmente todos los archivos tracked modiﬁcados
    - **git stash pop** --> Restaura los archivos guardados más recientemente
    - **git stash list** --> Enumera todos los sets de cambios en guardado rápido
    - **git stash drop** --> Elimina el set de cambios en guardado rápido más reciente
    <u>

- ### SINCRONIZAR CAMBIOS</u>
    - **git fetch [bookmark]** --> Descarga todo el historial del marcador del repositorio
    - **git merge [bookmark]/[branch]** --> Combina la rama del marcador con la rama local actual
    - **git push [alias] [branch]** --> Carga todos los commits de la rama local al GitHub
    - **git pull** --> Descarga el historial del marcador e incorpora cambios