# Instalando o Modem 3G no Raspberry Pi

Antes de começar, conecte o modem 3G no Raspberry Pi.

Ligar o Raspberry Pi e conectá-lo na rede. Efetuar um conexão ssh.

>Exemplo abaixo é utilizado se você estiver utilizando um Linux ou um Mac. Para usuários do Microsoft Windows recomendamos o uso do Putty.

```
ssh pi@<ip do raspberry>
```


Sempre recomendo a atualização dos pacotes antes de iniciar:

```
sudo apt-get update
```

1. Instalar o pacote "ppp" através do comando abaixo:

```
sudo apt-get install ppp
```

2. Baixar o sakis3g para o Raspberry Pi:

```
wget "http://raspberry-at-home.com/files/sakis3g.tar.gz"
```

A sugestão aqui é copiar o sakis3g para o /usr/bin/modem3d e descompactá-lo:

```
sudo mkdir /usr/bin/modem3g
sudo chmod 777 /usr/bin/modem3g
sudo cp sakis3g.tar.gz /usr/bin/modem3g
cd /usr/bin/modem3g
sudo tar -zxvf sakis3g.tar.gz
sudo chmod +x sakis3g
```

```
sudo ./sakis3g connect
Please select APN by using APN variable, or by enabling interactive mode.
        $ /usr/bin/modem3g/sakis3g --interactive "connect"

Available options are:
Internet         (Internet)
CUSTOM_APN      Custom APN...

Example:
        $ /usr/bin/modem3g/sakis3g APN="Internet"
```

```
APN="Internet"
```

```
sudo ./sakis3g connect
E220 connected to PLAY (26006).
```

```
sudo ./sakis3g disconnect
Disconnected.
```

```
/usr/bin/modem3g/sakis3g --interactive "menu" "console"
```
