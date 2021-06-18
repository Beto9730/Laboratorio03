# Laboratorio03

## A continuacion mostramos el proceso de elaboracion de 2 ramas PRUEBA 01 Y PRUEBA 02 y el ***merge*** en ambas ramas. 

>Elementos necesarios para el desarrollo del Laboratorio01:

- GIT Bash

Pasos a seguir para la creacion del Laboratio01:

>1. Clonamos el repositorio creado desde nuestro Git Hub
`````
git clone https://github.com/Beto9730/Laboratorio03.git
`````
>2. Creamos y nos direccionamos a la rama **PRUEBA01**
`````
$ git checkout -b PRUEBA01
Switched to a new branch 'PRUEBA01'
`````
>3. Creamos y configuramos el archivo PRUEBA y copiamos el contenido
`````
$ touch PRUEBA

git branch
git logs
git status
git commit
git add
git blame
git stash
git checkout -b RAMA
git diff
`````
>4. Validamos el estado del repositorio
`````
$ git status
On branch PRUEBA01
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        PRUEBA

no changes added to commit (use "git add" and/or "git commit -a")
`````
>5. Añadimos los cambios efectados 
`````
$ git add README.md PRUEBA
warning: LF will be replaced by CRLF in PRUEBA.
The file will have its original line endings in your working directory
`````
>6. Acontinuacion validamos el status de los cambios añadidos y validamos que se hayan añadido de manera correcta
`````
$ git status
On branch PRUEBA01
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   PRUEBA
        modified:   README.md

`````
>7. Añadimos los commit y comentarios que hayamos realizado 
`````
$ git commit -m "se añadio archivo PRUEBA en la rama PRUEBA01 y README.md en la rama main"
[PRUEBA01 77e1662] se añadio archivo PRUEBA en la rama PRUEBA01 y README.md en la rama main
 2 files changed, 9 insertions(+), 2 deletions(-)
 create mode 100644 PRUEBA

`````
>8. Por ultimo subimos los cambios al repositorio remoto
`````
$ git push origin PRUEBA01
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (4/4), 406 bytes | 406.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'PRUEBA01' on GitHub by visiting:
remote:      https://github.com/Beto9730/Laboratorio03/pull/new/PRUEBA01
remote:
To https://github.com/Beto9730/Laboratorio03.git
 * [new branch]      PRUEBA01 -> PRUEBA01
 
`````
>9. Validamos en el log todos los commit realizados  

`````
$ git log
commit 31d6c71fe5212c201fe60edec0a610c25492bc51 (HEAD -> PRUEBA02)
Author: Alberto Urquiza <aleduurna@gmail.com>
Date:   Thu Jun 17 15:13:44 2021 -0500

    se añadio archivo PRUEBA en la rama PRUEBA02

commit 77e16625dbd1e352b6ae0550f43f2cb0eb03d266 (PRUEBA01)
Author: Alberto Urquiza <aleduurna@gmail.com>
Date:   Thu Jun 17 15:10:03 2021 -0500

    se añadio archivo PRUEBA en la rama PRUEBA01 y README.md en la rama main

commit 17c18d15f6e5e88a26e6ad839b5d48cdeb8ab798 (origin/main, origin/HEAD, main)
Author: albertourquiza <53110065+Beto9730@users.noreply.github.com>
Date:   Thu Jun 17 14:51:57 2021 -0500

    Initial commit

`````
>10. Ejecutamos merge de PRUEBA02 en PRUEBA01 (antes nos ubicamos en la rama PRUEBA01 con git checkout PRUEBA01)
`````
$ git merge PRUEBA02
Merge made by the 'recursive' strategy.
 PRUEBA | 3 ---
 1 file changed, 3 deletions(-)

`````
>11. Por ultimo para verlo de manera grafica ejecutamos el comando en cada rama 
`````
$ git log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold cyan)%aD%C(reset) %C(bold green)(%ar)%C(reset)%C(bold yellow)%d%C(reset)%n''          %C(white)%s%C(reset) %C(dim white)- %an%C(reset)' --all


*   e6f7df9 - Thu, 17 Jun 2021 17:26:08 -0500 (49 minutes ago) (HEAD -> main, origin/main, origin/HEAD)
|\            Se agrego README.md a main - Alberto Urquiza
| * 5d6ed61 - Thu, 17 Jun 2021 15:17:35 -0500 (3 hours ago)
| |           Update README.md - albertourquiza
* |   45e8437 - Thu, 17 Jun 2021 15:26:52 -0500 (3 hours ago) (PRUEBA01)
|\ \            Merge branch 'PRUEBA02' into PRUEBA01 SE REALIZO EL MERGE DE PRUEBA02 EN PRUEBA01 - Alberto Urquiza
| * | b2c34cb - Thu, 17 Jun 2021 15:19:06 -0500 (3 hours ago) (origin/PRUEBA02, PRUEBA02)
| | |           se elimino archivo README de la rama PRUEBA02 - Alberto Urquiza
| * | 31d6c71 - Thu, 17 Jun 2021 15:13:44 -0500 (3 hours ago)
| | |           se añadio archivo PRUEBA en la rama PRUEBA02 - Alberto Urquiza
* | | 5250a38 - Thu, 17 Jun 2021 15:24:34 -0500 (3 hours ago) (origin/PRUEBA01)
|/ /            se elimino el archivo README.md de la rama PRUEBA01 - Alberto Urquiza
* / 77e1662 - Thu, 17 Jun 2021 15:10:03 -0500 (3 hours ago)
|/            se añadio archivo PRUEBA en la rama PRUEBA01 y README.md en la rama main - Alberto Urquiza
* 17c18d1 - Thu, 17 Jun 2021 14:51:57 -0500 (3 hours ago)
            Initial commit - albertourquiza

`````


