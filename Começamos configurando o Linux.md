Começamos configurando o Linux

#Linux

##Instalar o apache2
```
sudo apt update
sudo install apache2
sudo service apache2 status
```

##Configurar página html
```
cd /var/www/html/pedrila.html

<html>
<head><title>Trabalho de Redes</title></head>
<body>
    <h1>Teste para o trabalho de redes</h1>
    <p>Esta página foi desenvolvida por: Andrisa, Matheus e Pedro</p>
</body>
</html>

```


##Instalar o proxy squid
```
sudo apt update
sudo apt install squid
sudo nano /etc/squid/squid.conf
```

##Bloquear sites de bet
```
sudo touch /etc/squid/sites_bloqueados.txt
sudo nano /etc/squid/sites bloqueados.txt

http_port 3128

acl sites bloqueados url_regex -i "/etc/squid/sites bloqueados.txt"
http_access deny sites bloqueados

deny_info http://192.168.0.0/pedrila sites_bloqueados
```

##Configurar IP Tables
```
sudo apt install iptables
sudo apt install iptables-persistent
sudo systemctl enable netfilter-persistent
route add - net 0.0.0.0 netmask 0.0.0.0 GW IP

sudo apt install net-tools

```

##Instalar um servidor SSH
```

```

#Windows

##Configurar proxy do mozilla firefox