Creando ramas  https://www.genbeta.com/desarrollo/manejo-de-ramas-de-desarrollo-con-git

# Tutorial Git

## Actualizar y subir a la Rama master

Si estas manejando un proyecto muy pequeño y quieres actualizar el repositorio y subir, puedes seguir los siguientes pasos, no es recomendado, lo ideal es crear una rama y luego fusionar las ramas.


1. Verificamos el estatus de git para ver los archivos que hemos modificado
   
   git status
   

2. Actualizamos

   git fetch


3. Bajamos la actualizacion

   git pull
   

4. Adjuntamos los archivos (leer Usando Add)

   git add .


5. Hacemos commit y escribimos un mensaje

   git commit -m "mensaje"
   

6. Subimos los cambios

   git push origin master

<br>


## Usando Checkout

Si deseas descartar archivos adjuntados en git para subir usamos git

   git checkout  nombre_del_archivo
   
<br>   
   
## Usando ADD
Con este comando podremos adjuntar archivos, conozco 3 formas de hacerlo

1. Si quieremos adjuntar archivos con carpetas y todo
   
   git add .
   
2. Adjuntar solo archivos 

   git add *
   
3. Adjuntar archivos especificos, para eso hacemos git status y vemos la ruta de cada archivo, por ejemplo si git  status      nos dice que el archivo /home/usuario/prueba.py /home/usuario/user.png  eso significa que son dos archivos que fueron        agregados, si solo queremos subir el archivo prueba.py, hacemos lo siguiiente
   
   git add /home/usuario/prueba.py

<br>
<br>
## Pasos para subir cambios a un proyecto donde trabajan varias personas

 
1. Tipeamos el siguiente comando para saber cuales son los archivos modificados
   
   git status
   
   
2. Adjuntamos los archivos que queremos subir seguidamente del siguiente comando

   git add 

 
3. Hacemos un commit y escribimos un mensaje

   git commit -m 'mensaje' 

 
4. Actualizamos, es posible que halla un cambio pendiente que no lo tengamos localmente

   git fetch 


5. Devolvemos el commit

   git reset --soft HEAD^ 
   
 
6. Guardamos los cambios del commit en la pila

   git stash save 'mensaje' 
 

7. Verificamos si se ha guardado y en que posicion, debe estar en la posicion 0
   
   git stash list   

 
8. bajamos los cambios y actualizamos el repositorio
   
   git pull

 
9. Aplicamos los cambios guardados en la pila

   git stash apply stash@{0} 


10. Agregamos nuevamente los archivos que vamos a subir

   git add
 

11. Hacemos un commit

   git commit -m 'mensaje'

 
 12. tipeamos un push para subir
   
   git push

