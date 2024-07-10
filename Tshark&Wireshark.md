# Instalacion de Tshark y Wireshark
## Actualización

**Descripción**: Actualiza la lista de paquetes disponibles y sus versiones, luego instala las últimas versiones de todos los paquetes actualmente instalados en el sistema.
```
sudo apt-get update && sudo apt-get upgrade -y
```

## instalacion de Tshark
**Descripción**: instala tshark en Ubuntu, solicita algunas confirmaciones adicionales
```
sudo apt-get install tshark -y
```
**Nota**: Antes de finalizar la instalación, se debe indicar si se dará permiso a los usuarios no privilegiados para capturar datos. Con esta configuración se puede ejecutar tshark pero no reconoce todas las interfaces si no se ejecuta con privilegios de superusuario (`sudo`)
```
sudo usermod -aG wireshark lesand
```
**Donde**:
- `sudo`: Ejecuta el comando con privilegios de superusuario.
- `usermod`: Es una herramienta para modificar las cuentas de usuario.
- `-aG`: Añade el usuario a un grupo sin eliminarlo de otros grupos. `-a` significa "append" (agregar) y `G` indica que se añade a un grupo.
- `wireshark`: Es el nombre del grupo al que se añadirá el usuario.
- `lesand`: Es el nombre del usuario que se añadirá al grupo `wireshark`.

**Descripción:** Este comando añade al usuario `lesand` al grupo `wireshark`, permitiéndole acceder a los recursos y permisos asociados a ese grupo.
