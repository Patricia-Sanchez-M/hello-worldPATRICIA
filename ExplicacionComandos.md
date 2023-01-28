# COMANDOS


## **git fork** <*repositorio*>
 - Se utiliza para crear una copia de un repositorio remoto en una cuenta personal. 
 - Es un comando esencial en GitHub y GitLab, ya que ambas son plataformas para para el control de versiones centralizadas.
 - Consiste en crear una copia del repositorio en tu cuenta personal y una conexión entre dicha copia personal y el repositorio original para que puedas contribuir con tus cambios si los otros colaboradores los aceptan (mediante git pull, por ejemplo).

Para realizar dicho fork, se accedió al repositorio que se quería clonar mediante el URL [https://github.com/ALUMNO-GITT-PAT-practica-1/](https://github.com/gitt-3-pat/hello-world) y se utilizó el siguiente botón en la esquina superior derecha:

![image](https://user-images.githubusercontent.com/97602170/214024294-85d3d540-e9cd-45eb-8a2a-0566debde2f1.png)




## **git clone** <*repositorio a clonar*>
- Crea una copia idéntica de un repositorio objetivo en un repositorio local.
- Todos los cambios que realices a partir de entonces son localmente; no tienes permiso para modificar los archivos originales del autor.
- Se diferencia del fork porque no es una herramienta para el control de cambios de un proyecto, sino para modificar los archivos clonados a tu libre disposición.

Para demostrar el funcionamiento de este comando, se clonó el repositorio mencionado anteriormente en un directorio temporal, ya que no se desea tener los archivos duplicados en el repositorio local:

![image](https://user-images.githubusercontent.com/97602170/215187039-11026f3d-3232-4b76-a503-b8333d3aabd7.png)




## **git status**
Este comando proporciona información sobre el estado actual de la rama donde se encuentra el directorio donde es ejecutado. Esto incluye información sobre archivos que se han modificado, agregado, eliminado, etc.

Por ejemplo, tras la creación de un fichero hola.txt y de escribir "hola" en él, el comando git status sirve para revelar que se han producido cambios en el directorio /workspaces/hello-worldPATRICIA:

![image](https://user-images.githubusercontent.com/97602170/215190360-aaef86a5-ef61-448b-ae4d-91ba1d0d4c81.png)

![image](https://user-images.githubusercontent.com/97602170/215190459-1b2895d4-3bee-44b0-aa4c-e9489ebc6883.png)




## **git add** <*archivos*>
- Los cambios en git tienen lugar en tres fases. En primer lugar, tienen que ser incluidos en un primer borrador. El parámetro del comando indica los archivos para los cuales se quiere registrar un cambio; si se pone un ".", quiere decir a todos los archivos del directorio en el que se encuentre.
- Este comando se podría entender como una zona intermedia donde se almacenan los cambios que se incluirán en el siguiente paso.

Tras haber creado el fichero hola.txt y haber escrito "hola", hay que confirmar los cambios en el borrador:

![image](https://user-images.githubusercontent.com/97602170/215191985-199f7c42-ffda-4a97-9423-fa9c30db261e.png)




## **git commit -m** <*descripción*> 
- Este comando es el segundo paso para hacer públicos unos cambios realizados en un repositorio.
- Sigue al comando anterior y su función es la de guardar los cambios realizados en los borradores en un repositorio.
- Es necesario poner el parámetro -m seguido de un título de la versión, preferentemente descriptivo.
- En este punto, los ficheros siguen siendo solo visibles para el creador en su repositorio local.

![image](https://user-images.githubusercontent.com/97602170/215193554-9c7872d2-90cb-4d27-8db0-b8858ccaf240.png)

Si en este momento volvemos a hacer un *git status*, observaremos que los cambios están actualizados, y que ya solo queda un último paso para que esos cambios se reflejen en el repositorio de forma pública. Este último paso se comentará en el apartado siguiente.

![image](https://user-images.githubusercontent.com/97602170/215283373-15987873-cb67-495c-8fc6-b657a2918f8f.png)




## **git push** 
- El último paso para reflejar cambios en un repositorio de forma pública.
- Se utiliza para subir los cambios de repositorios locales a repositorios remotos en GitHub.
- Cabe destacar que solo se subirán los cambios de la rama especificada al repositorio remoto.
- Toma dos argumentos: 
  - El primero es el nombre del repositorio remoto al que se quiere subir los cambios.
  - El segundo es el nombre de la rama a la que se quiere subir los cambios.

En la imagen siguiente, se observa como *git push origin main* sube los cambios de la rama *main* del repositorio local al repositorio remoto llamado *origin*.

![image](https://user-images.githubusercontent.com/97602170/215283679-ae2b2392-7fb1-44d2-b941-d5377a9de9cd.png)

Además, tras este paso en mi repositorio remoto *origin*, aparece como cabía esperar el fichero hola.txt:

![image](https://user-images.githubusercontent.com/97602170/215283745-67eabb82-555f-4c4e-bc8b-4912e1690abe.png)




## **git checkout**
- Comando esencial para trabajar con ramas en un repositorio en GitHub.
- Con el parámetro -b y <*nombre de la rama*>, se crea una nueva rama, y se cambia a ella:

![image](https://user-images.githubusercontent.com/97602170/215284156-f41ea8e6-ccc7-4642-bcec-8c9fa2b617dd.png)

Aprendemos en esta imagen que en verde aparece el nombre de usuario de GitHub, en azul el nombre del repositorio remoto, y en rojo la rama en la que se encuentra.

- Para movernos de una rama a otra, utilizamos: *git checkout* <*nombre de la rama*>:

![image](https://user-images.githubusercontent.com/97602170/215284256-e1ef0119-1cf6-4673-8c26-6ad30435b315.png)



## **git branch**
- Otro de los comandos útiles para trabajar con ramas en GitHub.
- Si se usa sin ningún parámetro, lista todas las ramas de un repositorio:

![image](https://user-images.githubusercontent.com/97602170/215284522-88843ac1-11a0-4571-8e66-ffb4a9705c66.png)

- Si se usa el parámetro -d y <*nombre de la rama*>, se borra la rama:

![image](https://user-images.githubusercontent.com/97602170/215284592-a6266361-1bf1-4068-afd9-f138c4a74205.png)



## **git pull** 
Es el comando contrario a *git push*, pues se utiliza para fusionar todos los cambios hechos en el repositorio remoto con el repositorio local.

Por ejemplo, a la hora de añadir imágenes o poner texto en negrita o cursiva, edité este README directamente en el repositorio remoto. Después de hacer un *commit* de los cambios en la rama local desde el repositorio remoto (primera imagen), tuve que hacer un *git pull* en el repositorio local (segunda imagen) para que los cambios se viesen reflejados en él.

![image](https://user-images.githubusercontent.com/97602170/215284905-0e0c8471-0bd0-4598-81e9-d05365885194.png)

![image](https://user-images.githubusercontent.com/97602170/215285021-0c1099d5-ad84-462f-ad8e-a9a4702532a3.png)





# INSTALACIÓN DE SOFTWARE

## Java

![image](https://user-images.githubusercontent.com/97602170/215285261-77322bde-8c7d-47e4-a04a-556f800a8a0d.png)

## Maven

![image](https://user-images.githubusercontent.com/97602170/215285164-bc599324-8c0c-42a8-a957-d3c31d4060fb.png)

## Visual Studio Code

![image](https://user-images.githubusercontent.com/97602170/215285248-35c53b73-1a05-4780-a7b9-f774be7a396a.png)

## Docker

![image](https://user-images.githubusercontent.com/97602170/215285134-837d1154-e38e-46c9-9422-d308341b8fad.png)


