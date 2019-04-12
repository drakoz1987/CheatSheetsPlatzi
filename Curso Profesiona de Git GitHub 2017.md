git Comando principal a utilizar en Git
    
    subcomandos:
    
        init nombre_repo crear repositorio dentro de la carpeta nombre_repo
        
        init crea el repositorio en la carpeta actual
        
        status revisa el estado de los archivo en el Working directory o si han sufrido cambios
        
        add agrega elementos al seguimiento
            add nombre_archivo agrega ese elemento en particular
            add -A agrega todos los elementos untracked que no estan en el .gitignore
            add . similar a A-
            add -n nombre_archivo confirma el archivo existe pero no lo agrega al staging
            
        rm remueve archivos de git
            rm --cached nombre_archivo remueve el archivo indicado del staging directory
            rm -f nombre_archivo remueve el archivo de git y lo elimina por completo
        
        commit compromete los archivos 
            -m "mensaje" anade un mensaje al commit, es recomendable ser explicito en el mensaje
            -m "nuevo mensaje" --amend permite enmendar un error en el commit anterior y reemplazarlo por el nuevo
            
        log muestra los commit hechos en el repositorio
            --oneline resume el detalle de un log a una linea
            --graph da un grafico de la historia en la que se han hecho los commits
            -numero mustra los ultimos numero d commits
                    
        tag crea etiquetas para los commits
            -a version -m  crea una etiqueta anotada con una string
            version crea una etiqueta ligera por ejemplo para asignar una version
            version SHA1_del_commit_a_etiquetar permite etiquetar commits pasados
            -d etiqueta permite borrar la etiqueta indicada
            -f etiqueta permite renombrar la etiqueta indicada 
            -f -a etiqueta -m mensaje permite cambiar una etiqueta por otra en este caso usando una etiqueta anotada
        
        diff sha1 muestra diferencias entre commits con el estado actual
        diff sha1 sha1 muestra diferencia entre dos commits
        
        reset permite cambiar la historia del repo 
            --soft sha1 elimina los cambios desde el commit indicado por el sha1 pero soft devuelve el commit a stage no elimina nada solo revierte eso.
            --mixed sha1 mixed saca el cambio del staging area no borra archivos 
        
        branch nombre permite crear una rama para no alterar la master y hacer los cambios que se deseen.
            -l listado de ramas
            -d nombre borra rama sin commits pendientes
            -D nombre borra rama sin importar commits pendientes
            -m nombre_anterior nombre nuevo renombra rama
            
        checkout nombre o sha1 permite ir a otras ramas u otros commits
            -b nombre crea una rama nueva y ns coloca en ella automaticamente
            
        merge nombre_rama permite unir la rama en la que se esta con la rama mencionada.  
        
        