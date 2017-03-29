# Usuarios y permisos
![Redes](header_redes.svg)

En sistemas tipo *nix los permisos que poseen los recursos del sistema son muy importantes en términos de seguridad. 

Cuando en GNU/Linux creamos un **usuario**, automáticamente se crea un **grupo** con el mismo nombre del usuario. Por defecto, el usuario pertenece a dicho grupo. Además, existen los **otros** usuarios del sistema. Esto se representa simbólicamente: 

|         | Usuario (User) | Grupo (Group) | Otros (Others) |
| ------- | -------------- | ------------- | -------------- |
| Símbolo | u              | g             | o              |

Por otro lado, existen los **permisos** que son: 

|         | Lectura (Read) | Escritura (Write) | Ejecucción (Execute) |
| ------- | -------------- | ----------------- | -------------------- |
| Símbolo | r              | w                 | x                    |
| Valor   | 4              | 2                 | 1                    |



* u** (User), que simboliza el usuario propietario del recurso, 
* **g** (Group), representa el grupo propietario del recurso,
* **o** (Others), que refieren al resto de los usuarios del sistema. 

Por otro lado, para cada nivel de organización, los permisos se representan de la siguiente manera: 

* **r** (Read), permiso de lectura
* **w** (Write) , permiso de escritura
* **x** (Execute), permiso de ejecucción





