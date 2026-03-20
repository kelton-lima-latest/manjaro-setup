# manjaro-setup

## Corrigir lentidão na velocidade de internet na rede sem fio

Desativar economia de energia

Intel sofre MUITO com isso no Linux.
```bash
sudo iw dev wlp9s0 set power_save off
```

Agora torne permanente:
```bash
sudo nano /etc/NetworkManager/conf.d/wifi-powersave.conf
```

Coloque:
```bash
[connection]
wifi.powersave = 2
```

Reinicie:
```bash
sudo systemctl restart NetworkManager
```
