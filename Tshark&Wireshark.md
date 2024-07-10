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
