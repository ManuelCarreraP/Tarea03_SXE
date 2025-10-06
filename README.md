# Tarea03_SXE
Manuel Carrera Pazó
## Apartado 1 
El primer paso será ajecutar este comando para descargar la imagen "apline" sin arrancarla:
```bash
docker pull apline
```
<img width="746" height="149" alt="image" src="https://github.com/user-attachments/assets/97ac2d37-fac0-4326-bfbf-ec20bbda171e" />
<br><br>
Ahora comprobaremos si esta en el equipo:


```bash
docker images
```
<img width="693" height="92" alt="image" src="https://github.com/user-attachments/assets/ce9ea08e-b9b4-4120-89b3-580d09e48a30" />  

## Apartado 2
Este comando creará y ejecutará un contenedor, pero como no le damos ningún comando, se cierra automáticamente:
```bash
docker run alpine
```
<img width="946" height="598" alt="image" src="https://github.com/user-attachments/assets/2b89e707-0108-4ad9-9e34-331a89664c04" />

<br><br>
Este comando muestra los contenedores y podremos ver el nombre asignado automaticamente:
```bash
docker ps -a
```
<img width="1127" height="137" alt="image" src="https://github.com/user-attachments/assets/e8bdec7c-f449-467d-9e17-b5b4804e12cd" />
Podemos ver que el nombre asignado automáticamente es: practical_poitras
