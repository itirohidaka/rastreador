# Instalando o Modem 3G no Raspberry Pi

Antes de começar, conecte o modem 3G no Raspberry Pi.

Ligar o Raspberry Pi e conectá-lo na rede. Efetuar um conexão ssh.

>Exemplo abaixo é utilizado se você estiver utilizando um Linux ou um Mac. Para usuários do Microsoft Windows recomendamos o uso do Putty.

```
ssh pi@<ip do raspberry>
```


Sempre recomendo a atualização dos pacotes antes de iniciar.

```
sudo apt-get update
```

```
sudo apt-get install ppp
```

```
wget "http://raspberry-at-home.com/files/sakis3g.tar.gz"
```

```
sudo mkdir /usr/bin/modem3g
sudo chmod 777 /usr/bin/modem3g
sudo cp sakis3g.tar.gz /usr/bin/modem3g
cd /usr/bin/modem3g
sudo tar -zxvf sakis3g.tar.gz
sudo chmod +x sakis3g
```
