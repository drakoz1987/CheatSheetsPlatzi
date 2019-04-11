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
            
        git log muestra los commit hechos en el repositorio
        
        
        