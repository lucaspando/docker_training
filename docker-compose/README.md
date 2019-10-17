##Importante

-El docker-compose utiliza el nombre del directorio como nombre del proyecto, por lo tanto si estamos parados en cualquier directorio y queremos hacer un docker-compose ps de un proyecto en particular, debemos agregarle el argumento -p <nombre_proyecto>

-Si queremos cambiar el nombre del archivo docker-compose.yml, lo podemos hacer pero al momento de correr el docker-compose up debemos agregar el argumento -f <nombre_archivo>

-Tambien podemos cambiarle el nombre del proyecto para que no tome el del directorio por defecto agregando el argumento -p <nombre_proyecto>