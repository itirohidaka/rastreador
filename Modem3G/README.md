# Instalando o Modem 3G no Raspberry Pi

Antes de começar, conecte o modem 3G no Raspberry Pi.

1. Ligar o Raspberry Pi e conectá-lo na rede. Efetuar um conexão ssh.

>Exemplo abaixo é utilizado se você estiver utilizando um Linux ou um Mac. Para usuários do Microsoft Windows recomendamos o uso do Putty.

```
ssh pi@<ip do raspberry>
```

2. Sempre recomendo a atualização dos pacotes antes de iniciar:

```
sudo apt-get update
```

3. Instalar o pacote "ppp" através do comando abaixo:

```
sudo apt-get install ppp
```

4. Baixar o sakis3g para o Raspberry Pi:

```
wget "http://raspberry-at-home.com/files/sakis3g.tar.gz"
```

5. A sugestão aqui é copiar o sakis3g para o /usr/bin/modem3d e descompactá-lo com os seguintes comandos:

```
sudo mkdir /usr/bin/modem3g
sudo chmod 777 /usr/bin/modem3g
sudo cp sakis3g.tar.gz /usr/bin/modem3g
cd /usr/bin/modem3g
sudo tar -zxvf sakis3g.tar.gz
sudo chmod +x sakis3g
```

6. Modificar o arquivo /etc/sakis3g.conf com o parâmetro APN. No meu caso estou utilizando uma linha pré-paga da Vivo portanto:

```
APN="Vivo"
```

7. Para realizar a conexão com a internet basta utilizar o comando abaixo:

```
sudo ./sakis3g connect
E220 connected to PLAY (26006).
```

8. Para desconectar basta utilizar o comando abaixo:

```
sudo ./sakis3g disconnect
Disconnected.
```
