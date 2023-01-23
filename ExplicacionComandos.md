git fork 
 - se utiliza para creae una copia de un repositorio remoto en una cuenta personal. 
 - es un comando esencial en GitHub y GitLab, ya que ambas son plataformas para para el control de versiones centralizadas.
 - se crea una copia del repositorio en tu cuenta personal y una conexión entre tu copia personal y el repositorio original para que puedas contribuir con       tus cambios si los otros colaboradores los aceptan (mediante git pull, por ejemplo).

Para realizar dicho fork, se accedió al repositorio que se quería clonar mediante el URL [https://github.com/ALUMNO-GITT-PAT-practica-1/](https://github.com/gitt-3-pat/hello-world) y se utilizó el siguiente botón:

![image](https://user-images.githubusercontent.com/97602170/214024294-85d3d540-e9cd-45eb-8a2a-0566debde2f1.png)





git clone:




En mi caso, clone el repositorio del cual hice fork en una carpeta temporal, para que no tener los archivos duplicados del fork en mi repositorio local:

@Patricia-Sanchez-M ➜ /workspaces/hello-worldPATRICIA (main) $ cd /tmp
@Patricia-Sanchez-M ➜ /tmp $ git clone https://github.com/gitt-3-pat/hello-world/
Cloning into 'hello-world'...
remote: Enumerating objects: 38, done.
remote: Counting objects: 100% (4/4), done.
remote: Compressing objects: 100% (4/4), done.
remote: Total 38 (delta 0), reused 0 (delta 0), pack-reused 34
Unpacking objects: 100% (38/38), 59.54 KiB | 1.86 MiB/s, done.


git status: este comando proporciona información sobre el estado actual de la rama donde se encuentra.
            esto incluye información sobre: archivos que se han modificado/agregado/eliminado




git add: se utiliza para agregar archivos o cambios a un "índice"/"staging area" (zona intermedia donde se almacenan los cambios que se incluirán en el siguiente commit).
         

git commit: este comando sigue al anterior y su función es confirmar los cambios realizados en un repositorio.

git push: 
