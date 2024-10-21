# 1. Determinar en qué archivos se encuentra la cadena <<PATH>>.
```sh
grep -r "PATH" /
```

# 2. Obtener todos los procesos del sistema.
```sh
ps -e
```

# 3. Obtener todos los procesos del usuario actual.
```sh
ps -u
```

# 4. Finalizar un proceso con un identificador de proceso dado.
```sh
kill <pid>
```

# 5. Finalizar todos los procesos que consisten en la ejecución de un determinado fichero ejecutable. 
??????????
```sh
killall nombre # Usando chatgpt
```

# 6. Lanzar el programa Firefox y matarlo desde una terminal.
??????

# 7. Verificar que el contenido de dos archivos coincide.
```sh
# chatgpt
cmp file1 file2 
diff file1 file2
```

# 8. Hacer que todos los archivos existentes en mi directorio actual sólo puedan ser ejecutados por su propietario.
```sh
#chatgpt
chmod u+x,go-x *
```

# 9. Crear un archivo vacío de nombre «prueba».
```sh
touch prueba
```

# 10. Cambiar la fecha de la última actualización al fichero <<prueba>> a 15/10/2002.
```sh
touch -t 0201150000
```

# 11. Cambiar el propietario del fichero «prueba»
```sh
chown <newuser> prueba
```

# 12. Cambiar el grupo propietario del fichero <<prueba>>.
```sh
chgrp <newgroup> prueba
```

# 13. Localizar a partir del directorio actual todos los archivos propiedad del usuario *root*.
```sh
find / -user root
```

# 14. Localizar todos los archivos en el sistema cuyo nombre contenga la cadena <<rc>>.
```sh
find / -name *rc*
```

# 15. Localizar todos los archivos del sistema que hayan sido modificados en el día de hoy.
```sh
find / -mtime -1
```

# 16. Borrar todos los ficheros regulares con extensión «.txt» del directorio «/tmp» que tengan más de dos días de antigüedad.
```sh
#chatgpt
find /tmp -type f -name "*.txt" -mtime +2 -delete
```