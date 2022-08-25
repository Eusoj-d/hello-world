# Generar un repositorio local y posteriormente unirlo a uno remoto

## Creación de repositorio

1. Inicializar *git bash*
2. Obtener la ruta de una carpeta determinada.
3. Ingresar el comando *git init*; esto crea una carpeta *.git* y con esto sabemos que el repositorio local a sido creado sin errores.

## Unir el repositorio local a uno remoto (ubicado en Github) y relizar cambios en la branch main

1. Declarar usuario y email
2. Con el comando *git add [nombreDelArchivo.sufijo]* se agrega un archivo a la "cola de espera"
3. Realizamos un **commit** o solicitud para realizar los cambios deseados mediante el siguiente comando *git commit -m "texto que describe la solicitud de cambio"*
   3.1 Se debe recibir un mensaje parecido a esto:
          [master (root-commit) cdbf084] primer commit
           1 file changed, 1 insertion(+)
           create mode 100644 prueba.txt
4. Se **conecta el repositorio local con uno remoto** mediante el siguiente comando *git remote add **origin** https://github.com/Eusoj-d/hello_world_public.git*; origin es el aleas con el que se identifica el repositorio remoto, se puede colocar cualquier nombre pero por lo general y buena práctica se coloca **origin** como aleas al repositorio remoto
5. Al estar en *git bash* nos encontramos por defecto en la *branch* o rama **master**, cambiamos de *branch master* a **branch main** porque esta es la rama que se encuentra por defecto en github con el comando *git branch -M main*
6. Posteriormente se ejecuta el comando *git push -u **origin** **main***; **origin** es el aleas del repositorio remoto y **main** es la rama en la que queremos hacer los cambios
    6.1 Debe aparecer un mensaje similiar a este:
          Enumerating objects: 3, done.
          Counting objects: 100% (3/3), done.
          Writing objects: 100% (3/3), 224 bytes | 224.00 KiB/s, done.
          Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
          To https://github.com/tuUsuario/nombreDeTuRepositorio
           * [new branch]      main -> main
          branch 'main' set up to track 'origin/main'.
