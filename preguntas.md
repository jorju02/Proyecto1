# Preguntas y Respuestas

## P-¿Cómo cambiar el mensaje de un commit?
### R- La opción más práctica y rápida es usar:  
    git commit --amend
### Tras lo cual se te abrirá el editor para que puedas modificar el mensaje.   

## P- Pull a un branch remoto que no existe en mi local
### R- Primero debes hacer un fetch
    git fetch <remoto> <rama>

### Fetch trae la rama remota, en el caso tuyo la de tu compañero y la almacena dentro de < remoto>/< rama>

### Pull es una combinación de 

    fetch+merge 
### Cuando hagas el fetch puedes hacer checkout a esa rama dentro del remoto sin mezclarla con alguna local y luego, hacer merge. Otra opción rápida también sería crear una rama localmente, hacer checkout a esa rama y luego hacer pull de la rama remota.

### El problema con pull como lo expresas en tu pregunta, es que hace tanto el fetch como un merge automático de esa rama a la rama donde está situado actualmente.


## P- Volver a commit anterior
### R- Puedes volver a una revisión antigua usando checkout y pasando el hash del commit. Por ejemplo:

    git checkout ab25f1ln2b4o3a9c4u1v6k4n1m7 .
### No olvides el punto al final. También puedes descartar cambios mediante reset pasándole el numero de commits. Por ejemplo, para descartar los últimos 3 commits:

    git reset --hard HEAD~3
### La diferencia entre checkout y reset es que en éste último se descartan las revisiones, mientras que con checkout se preservan.


## P-¿Para qué se usan los tags en Git?
### R-Sirven para dejar un registro, una marca de una versión en concreto. Se hacen cuando publicas una versión (v0.1, v1.0, v2.2, etc.) de modo que puedas volver a dicha versión por si tuvieras que probar alguna funcionalidad o error que suceda en esa versión


## P-¿Cómo ver qué archivos son diferentes entre 2 ramas con Git?
### R-Básicamente el comando para ver las diferencias entre dos branches es:

    git diff branch1..branch2
### Para listar qué archivos han cambiado entre dos branches puedes usar --name-status:

    git diff --name-status branch1..branch2


## P-¿Qué es la rama master en git?
### R-Cuando clonas un repositorio clonas también sus ramas, no sólo la master (la maestra, la que se crea por defecto), pero las guarda dentro del repositorio "remoto" y no la hace "local" hasta que usemos checkout.

### Usando git branch -a podrás ver todas y usando git checkout todo podrás cambiar a la rama todo y ver que cambia el contenido del repositorio, momento a partir del cual también podrás ver esa rama como local usando git branch -a.

## P-Git me pide contraseña cada vez que envío a Github
### R-Intenta con...

    git config --global credential.helper wincred
### Te solicitará las credenciales una vez y quedaran cacheadas para futuras operaciones.

