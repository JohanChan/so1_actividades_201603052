### Ejercicio 4
Script para servicio
```
#!/bin/bash

fecha=$(date)
echo "$fecha"
echo "Hola desde servicio"
```

Se crea el servicio
```
sudo /etc/systemd/system/ejercicio4.service
```

Se abre el archivo de nuestro servicio
```
[Unit]
Description=Ejercicio 4
After=systend-user-sessions.service

[Service]
Type=simple
ExecStart=/home/ldev/Documentos/sopes/ejercicio4.sh
```

Ejecutar servicio
```
sudo systemctl start ejercicio4.service
```

Estado de servicio
```
systemctl status ejercicio4
```

Historial del servicio
```
journalctl -u ejercicio4 -e
```
