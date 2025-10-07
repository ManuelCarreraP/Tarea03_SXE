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

## Apartado 3
Con este comando crearemos un contenedor con el nombre 'dam_alp1'.
```bash
docker run -it --name dam_alp1 alpine sh
```
Explicacion parámetros:  
· **-it**: permite abrir una sesión interactiva.  
· **--name dam_alp1**: asigna nombre al contenedor.  
· **sh**: abre la shell dentro del contenedor.  

<img width="710" height="54" alt="image" src="https://github.com/user-attachments/assets/0c049fe6-8de0-4a59-b255-828e41a6a6af" />

## Apartado 4
Primero si no tenemos la sesión abierta del contenedor dam_alp1 la abrimos con el siguiente comando:
```bash
docker start -ai dam_apl1
```  
Ahora ejecutamos ip addr para conocer la IP, en mi caso **172.17.0.2/16**
<img width="875" height="735" alt="Captura desde 2025-10-07 08-48-09" src="https://github.com/user-attachments/assets/c25ac108-119c-4e5f-95b8-94a2cd0ee896" />
<br><br>
A continuacion le haremos ping a google.com
```bash
ping -c 4 google.com
```
<img width="612" height="243" alt="Captura desde 2025-10-06 11-49-53" src="https://github.com/user-attachments/assets/73fa8b72-b966-42f4-981e-bf1151b612b8" />

## Apartado 5
Creamos el segundo contenedor con el mismo comando que usamos en el anterior:
```bash
docker run -it --name dam_alp2 alpine sh
```
A continuacion haremos ping a la IP del primer contenedor (**172.17.0.2**) desde nuestro nuevo contenedor que tiene la IP **172.17.0.3**  
```bash
ping -c 4 172.17.0.2
```
<img width="616" height="287" alt="image" src="https://github.com/user-attachments/assets/1f4898d5-006d-4cb9-a2e9-833727085698" />
