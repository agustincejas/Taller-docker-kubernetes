## HEALTHCHECK
Permite indicarle a Docker cómo validar que el contenedor está corriendo correctamente. Por default sólo
valida que esté corriendo, por lo que puede estar corriendo y devolviendo respuestas erróneas.

Modos:
	
	HEALTHCHECK [OPTIONS] CMD command
  	HEALTHCHECK NONE

Con este comando se tiene más control sobre la salud del container.
Sólo puede haber un HEALTHECK por Dockerfile, si hay más se toma el último.
Se especifica un comando a correrse dentro del contendor cuyo valor resultante determinará el estado.
Valores posibles: 
* 0: success -> healthy	
* 1: unhealthy
* 2: reserved  

Puede verse con docker inspect el output producido por el comando para debuggear.

## ONBUILD

Especifica acciones para ejecutarse cuando la imagen sea usada como base de otra, es decir en una clásula FROM.

Sirve para proveer una especie de template, cuando es útil correr una serie de comandos luego de traer la imagen. Si falla alguno de los comandos especificados aquí, falla la cláusula FROM.


## VOLUME
Crea un punto de montura  en el contenedor.

Son usados para persistir data generada y usada por contenedores.

Pueden declararse dentro del Dockerfile "VOLUME" o al correr el container con -v o --mount, donde --mount permite más flexibilidad sobre las opciones del mismo.