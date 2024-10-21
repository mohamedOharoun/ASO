# 1. Mostrar un listado en pantalla con el primer y el quinto campo de todas las líneas del fichero «/etc/passwd».
```sh
cut -d : -f 1,5 /etc/passwd
```

# 2. Mostrar un listado en pantalla que contenga desde el primer *byte* hasta el tercero y desde el quinto hasta el octavo del fichero <</etc/passwd>>
```sh
cut 1-3,5-8 /etc/passwd
```

# 3. Mostrar un listado en pantalla que contenga con el primer y el quinto campo de todas las líneas del fichero <</etc/passwd>>. El listado debe estar ordenado alfabéticamente por el segundo campo.
```sh
#chatgpt
cut -d : -f 1,5 /etc/passwd | sort -k2
```

# 4. Mostrar un listado en pantalla con el primer, el tercer y el quinto campo de todas líneas del fichero <</etc/passwd>>. El listado debe estar ordenado por el identificador de usuario.
```sh
# chatgpt
cut -d : -f 1,3,5 /etc/passwd | sort -t : -k2,2n
```

# 5. Mostrar un listado en pantalla con el primer, el tercer y el quinto campo de todas las líneas del fichero "/etc/passwd". El listado debe estar ordenado por el contenido de los caracteres 2, 3 y 4 de cada línea.
```sh
# chatgpt
cut -d : -f 1,3,5 /etc/passwd | sort -k1.2,1.4
```

# 6. Mostrar un listado con el primer y el quinto campo del fichero «/etc/passwd» que incluya solamente aquellas líneas que contienen la cadena «root». El listado estará ordenado alfabéticamente por el primer campo.
```sh
cut -d : -f 1,5 /etc/passwd | grep root | sort -k1
```

# 7. Mostrar un listado ordenado por el identificador de usuario de todas las líneas del fichero «/etc/passwd» que contienen la cadena «bash».
```sh
cut -d : -f 1-7 /etc/passwd | grep bash
```

# 8. Mostrar un listado numerado de todas las líneas del fichero «/etc/passwd» que contienen la cadena «bash».
```sh
cut -d : -f 1-7 /etc/passwd | grep bash | nl
```

# 9. Mostrar el número de líneas del fichero «/etc/passwd» que contienen la cadena «bash».
```sh
cut -d : -f 1-7 /etc/passwd | grep bash | wc -l
```