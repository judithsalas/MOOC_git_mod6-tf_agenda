# MOOC_git_mod6-tf_agenda
## Práctica 6
*Judith M.ª Salas García*
Para la elaboración del módulo 6 se han seguido los siguientes pasos:
En primer lugar, se realizó "fork" del repositorio **MOOC_git_mod6-tf_agenda** a través de github para posteriormente clonarlo en nuestra consola y trbajar con él de forma local (**git clone "la URL de nuestro <<fork>>-"**).
Una vez clonado el repositorio en nuestro ordenador, se navegó hasta el directorio de interés, **MOOC_git_mod6-tf_agenda**, a través del comando **cd MOOC_git_mod6-tf_agenda**, y se comenzaron a efectuar los primeros cambios.
Al ver los commits previamente llevados a cabo con **git log --oneline**, se podía observar que había dos commits referentes al teléfono de "Eva", lo cual se solucionó juntándolos en uno solo. 
Había un segundo error en el repositorio, se debía cambiar el número de Mary en el archivo **tf_agenda.txt**. 
Se modificaron estos dos "errores" mediante un **git rebase -i HEAD~3**. Una vez se introdujo el comando se abrió un editor donde se encontraban los tres últimos commits con la palabra "pick" delante, cambiando en "Add teléfono solo Eva" el pick por squash y en "Add teléfono Mary" por un edit. Para el guardado y el cierre del editor de texto (vi) se pulsó "esc" y a continuación, ":wq".
Una vez cerrado el editor, git integra los dos commits de forma automática y abre un nuevo editor de texto para que se modifiquen los mensajes de los commits.
En el primer commit se introdujo "Add Eva tf integrated" y en el segundo "Add Eva pending-tf", después se cerró el editor. 
En el siguiente paso se editó el fichero tf_agenda.txt con **nano tf_agenda.txt** cambiando, una vez dentro, el teléfono de Mary. Depués de la modificación, se añadieron los cambios con **git add tf_agenda.txt**.
Y para cambiar el commit del teléfono de Mary se utilizó **git commit --amend**, que al insertarlo nos abrió otro editor donde añadimos al final del mensaje del commit inicial, un "fixed" y se cerró el editor (esc :wq) para finalizar con el amend.
Una vez contamos con el mensaje de confirmación continuamos con el rebase (**git rebase --continue**), donde se nos confirmó que se habían producido los cambios.

Por último se introdujeron los cambios realizados en la rama master local a una nueva rama que fue llamada como corrected_tf_agenda. Para crearla y trabajar en ella se utilizó **git checkout -b corrected_tf_agenda** y para introducir los cambios al repositorio remoto se introdujo **git push origin corrected_tf_agenda**.

