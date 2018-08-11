## Usando Checkout

Si deseas sacar archivos adjuntados en git para subir usamos git

   git checkout  nombre_del_archivo

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
   
 
6- Guardamos los cambios del commit en la pila

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

