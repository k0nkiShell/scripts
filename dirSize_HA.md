## 🛠️ Pasos Posteriores {{ dirSize_HA }}

``` bash
#Creamos la variable de entorno con el token de HA
sudo nano /etc/ha.env

#Dentro del archivo /etc/ha.env, añade esta línea (reemplaza con tu token real):

HA_TON="eyJhb........................"

#Damos permisos de ejecución al script
chmod +x dirSize.sh
sudo chmod 700 /root/dirSize.sh

#Abrimos crontab
crontab -e

#En el editor de crontab, añade la siguiente línea para que el script se ejecute cada 5 minutos:

*/5 * * * * /root/dirSize.sh

# Reiniciamos el servicio cron y verificamos su estado
sudo systemctl restart cron.service
sudo systemctl status cron.service
```
📅 Puedes verificar o ajustar el formato del cron con esta herramienta:
🔗 https://crontab.guru/#/5_*_
