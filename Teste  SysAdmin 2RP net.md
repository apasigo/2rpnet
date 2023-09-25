```

2RP Net
Teste SysAdmin

```

```
A Nuven Publica utilizada foi a GCC da google.
Links de acessos:

Grafana: http://35.185.198.51:3000/
Xampp:   http://35.185.198.51:41062/

OBS: Foram criadas regras dentro do firewall para a liberação das portas de acesso.
```

```
Instalação do Docker 
A instalação foi padão seguindo o site " https://docs.docker.com/engine/install/debian/  " 

Abaixo a validação dos containers rodando 
octavio_a_neto@teste-2rp-net:~$ sudo docker ps
CONTAINER ID   IMAGE                        COMMAND            CREATED       STATUS       PORTS                                                                                        NAMES
653831616cc4   grafana/grafana-enterprise   "/run.sh"          2 hours ago   Up 2 hours   0.0.0.0:3000->3000/tcp, :::3000->3000/tcp                                                    grafana
f9ed5c0b5fad   tomsik68/xampp:8             "sh /startup.sh"   2 hours ago   Up 2 hours   3306/tcp, 0.0.0.0:41061->22/tcp, :::41061->22/tcp, 0.0.0.0:41062->80/tcp, :::41062->80/tcp   myXampp
octavio_a_neto@teste-2rp-net:~$ 
```

```
Validação do Mysql
octavio_a_neto@teste-2rp-net:~$ sudo mysql -uroot -p
Enter password: 
Welcome to the MariaDB monitor.  Commands end with ; or \g.
Your MariaDB connection id is 190
Server version: 10.5.19-MariaDB-0+deb11u2 Debian 11

Copyright (c) 2000, 2018, Oracle, MariaDB Corporation Ab and others.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

MariaDB [(none)]> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| performance_schema |
| zabbix             |
+--------------------+
4 rows in set (0.008 sec)

MariaDB [(none)]> 
```

``` 
Instalação do Xampp conforme exemplo do Site:https://hub.docker.com/r/tomsik68/xampp/

Validação no item acima " Validação dos containers rodando "

```

```
Item de Criação da dashboard infelizmente não foi concluido.
Tive problema para integra ele tanto com a API do "Google Cloud Monitoring". 
Quanto pelo Plugin do Zabbix, que foi instalado como alternativa.

O zabbix não tem integração com o Grafana 10 no momento. 
E a API do Google, não estava me trazando as informações para a criação da dashboard por mais que ela senha se conectado.

```

```
Sobre a Regra de aberta, as mesmas foram criadas dentro do Zabbix instalado na instancia e dentro do monitoring do GCC como redundancia. 
```

```
Tarefa 8
Foi realizado a criação dos usuarios e senhas , e liberado os acessos conforme solicitado
sysadmin@2rpnet.com - ZP1NQ(pZE=(k
academy@2rpnet.com  - PpHcv{~$E4Yu
people@2rpnet.com   - CdSy<$U/(QRs
```

```
Valores do projeto.

O projeto em andamento ficou com um custo somente de US$14.89 dolares por mês , pois foi utilizado uma simples.

Para o projeto de produção recomendo:

Pague pelo que usar: faturamento por segundo e sem custos iniciais

Item:

Estimativa mensal
2 vCPU + 8 GB memory	            - US$ 69,47	
Computação confidencial	          - US$ 12,29	
Disco permanente padrão de 20 GB	- US$ 0,88	
Total	                            - US$ 82,64


```