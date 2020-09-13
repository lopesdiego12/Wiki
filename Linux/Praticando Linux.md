##### Pré requisitos

Veja [Docker Install](https://docs.docker.com/docker-for-windows/install/) **Logar e docker estar com status running**



##### Ubuntu docker

```
docker search ubuntu
```
```
docker pull ubuntu
```
```
docker images
```
```
docker ps -l
```
```
docker run ubuntu
```
```
docker run -i -t ubuntu /bin/bash
```

##### Referência - https://lisha.ufsc.br/dl2172

##### Listando conteudo
```
ls (list directory contents)

root@3c435b57cbf2:/# ls
bin  boot  dev  etc  home  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
```
```
ls -ltrh

root@3c435b57cbf2:/# ls -ltrh
total 64K
drwxr-xr-x   8 root root 4.0K May 23  2017 lib
drwxr-xr-x   2 root root 4.0K Apr 24  2018 home
drwxr-xr-x   2 root root 4.0K Apr 24  2018 boot
drwxr-xr-x   1 root root 4.0K Mar 11 21:03 usr
drwxr-xr-x   2 root root 4.0K Mar 11 21:03 srv
drwxr-xr-x   2 root root 4.0K Mar 11 21:03 opt
drwxr-xr-x   2 root root 4.0K Mar 11 21:03 mnt
drwxr-xr-x   2 root root 4.0K Mar 11 21:03 media
drwxr-xr-x   2 root root 4.0K Mar 11 21:03 lib64
drwxr-xr-x   1 root root 4.0K Mar 11 21:05 var
drwx------   2 root root 4.0K Mar 11 21:05 root
drwxr-xr-x   2 root root 4.0K Mar 11 21:05 bin
drwxrwxrwt   2 root root 4.0K Mar 11 21:05 tmp
drwxr-xr-x   1 root root 4.0K Mar 20 19:20 sbin
drwxr-xr-x   1 root root 4.0K Mar 20 19:20 run
drwxr-xr-x   1 root root 4.0K Apr 16 00:10 etc
dr-xr-xr-x 125 root root    0 Apr 16 00:10 proc
dr-xr-xr-x  13 root root    0 Apr 16 00:10 sys
drwxr-xr-x   5 root root  360 Apr 16 00:10 dev
```
```
ls -ltrhF

root@3c435b57cbf2:/# ls -ltrhf
lib  dev  opt  boot  root  media  sbin  sys  ..  mnt  .  tmp  home  run  srv  etc  usr  proc  var  bin  lib64  .dockerenv
```
```
ls -la

root@3c435b57cbf2:/# ls -la
total 72
drwxr-xr-x   1 root root 4096 Apr 16 00:10 .
drwxr-xr-x   1 root root 4096 Apr 16 00:10 ..
-rwxr-xr-x   1 root root    0 Apr 16 00:10 .dockerenv
drwxr-xr-x   2 root root 4096 Mar 11 21:05 bin
drwxr-xr-x   2 root root 4096 Apr 24  2018 boot
drwxr-xr-x   5 root root  360 Apr 16 00:10 dev
drwxr-xr-x   1 root root 4096 Apr 16 00:10 etc
drwxr-xr-x   2 root root 4096 Apr 24  2018 home
drwxr-xr-x   8 root root 4096 May 23  2017 lib
drwxr-xr-x   2 root root 4096 Mar 11 21:03 lib64
drwxr-xr-x   2 root root 4096 Mar 11 21:03 media
drwxr-xr-x   2 root root 4096 Mar 11 21:03 mnt
drwxr-xr-x   2 root root 4096 Mar 11 21:03 opt
dr-xr-xr-x 125 root root    0 Apr 16 00:10 proc
drwx------   2 root root 4096 Mar 11 21:05 root
drwxr-xr-x   1 root root 4096 Mar 20 19:20 run
drwxr-xr-x   1 root root 4096 Mar 20 19:20 sbin
drwxr-xr-x   2 root root 4096 Mar 11 21:03 srv
dr-xr-xr-x  13 root root    0 Apr 16 00:44 sys
drwxrwxrwt   2 root root 4096 Mar 11 21:05 tmp
drwxr-xr-x   1 root root 4096 Mar 11 21:03 usr
drwxr-xr-x   1 root root 4096 Mar 11 21:05 var
```

##### Navegando nos diretórios
```
cd (change directory)

root@3c435b57cbf2:/# cd home/
root@3c435b57cbf2:/home#

root@3c435b57cbf2:/home# cd ..
root@3c435b57cbf2:/#

```
##### Exibindo mensagem no terminal
```
echo (display a line of text)

root@3c435b57cbf2:/# echo ~
/root

root@3c435b57cbf2:/home# echo Essa mensagem passa cinco argumentos
Essa mensagem passa cinco argumentos

root@3c435b57cbf2:/home# echo "A mensagem entre aspas passa um argumento"
A mensagem entre aspas passa um argumento
```

##### Retornando o diretório em que estamos
```
pwd ( print name of current/working directory)

root@3c435b57cbf2:/home# pwd
/home

```

##### Criando arquivo
```
touch (change file timestamps)

root@3c435b57cbf2:/home# touch teste.txt
root@3c435b57cbf2:/home#
```

##### Confira o arquivo criado 
```
root@3c435b57cbf2:/home# ls -ltrh
total 0
-rw-r--r-- 1 root root 0 Apr 16 01:03 teste.txt
```

##### Criando arquivo com echo
```

root@3c435b57cbf2:/home# echo "Bem vindo!" > teste2.txt
root@3c435b57cbf2:/home#

root@3c435b57cbf2:/home# ls -ltrh
total 4.0K
-rw-r--r-- 1 root root  0 Apr 16 01:03 teste.txt
-rw-r--r-- 1 root root 11 Apr 16 01:08 teste2.txt  
```

##### Inserindo informações em um arquivo
```
root@3c435b57cbf2:/home# echo "Ola!" >> teste2.txt
root@3c435b57cbf2:/home#
```
##### Exibindo o conteúdo de um arquivo
```
cat (concatenate files and print on the standard output)

root@3c435b57cbf2:/home# cat teste2.txt
Bem vindo!
Ola!
```
##### Removendo arquivo
```
rm (remove files or directories)

root@3c435b57cbf2:/home# ls
teste.txt  teste2.txt

root@3c435b57cbf2:/home# rm teste.txt

root@3c435b57cbf2:/home# ls
teste2.txt

```
##### Criando diretorio
```
mkdir (make directories)

root@3c435b57cbf2:/home# mkdir workspace
root@3c435b57cbf2:/home# ls
teste2.txt  workspace
```
```
mkdir -p /temp/temp1/temp2
```
##### Copiando arquivo
```
cp (copy files and directories)

root@3c435b57cbf2:/home# ls
teste2.txt  workspace
root@3c435b57cbf2:/home# cp teste2.txt copiateste2.txt
root@3c435b57cbf2:/home# ls
copiateste2.txt  teste2.txt  workspace
```
##### Copiando para dentro de um diretório
```
root@3c435b57cbf2:/home# cp *txt workspace
root@3c435b57cbf2:/home# cd workspace/
root@3c435b57cbf2:/home/workspace# ls
copiateste2.txt  teste2.txt

```

##### Renomenando arquivo (não disponível no Docker)
##### Talvez seja necessário instalar (será pedida a senha do root), no Ubuntu digite:
```
~$ sudo apt-get install rename
```
##### Renomeando miltiplos arquivos
```
rename (rename multiple files)

username@username:~/Documentos$ ls
lista.txt

username@username:~/Documentos$ touch teste.txt teste1.txt teste3.txt

username@username:~/Documentos$ ls
lista.txt  teste1.txt  teste3.txt  teste.txt

username@username:~/Documentos$ rename 's/.txt/.doc/' *.txt
username@username:~/Documentos$ ls
lista.doc  teste1.doc  teste3.doc  teste.doc

```

##### Criando link simbolico
```
ln (make links between files)

ln -s

root@3c435b57cbf2:/# ln -s /home/workspace/dir1/ dir1

root@3c435b57cbf2:/# ls -l
total 72
drwxr-xr-x   2 root root 4096 Mar 11 21:05 bin
drwxr-xr-x   2 root root 4096 Apr 24  2018 boot
drwxr-xr-x   5 root root  360 Apr 16 00:10 dev
lrwxrwxrwx   1 root root   21 Apr 16 02:19 dir1 -> /home/workspace/dir1/
drwxr-xr-x   1 root root 4096 Apr 16 00:10 etc
drwxr-xr-x   1 root root 4096 Apr 16 02:17 home
drwxr-xr-x   8 root root 4096 May 23  2017 lib
drwxr-xr-x   2 root root 4096 Mar 11 21:03 lib64
drwxr-xr-x   2 root root 4096 Mar 11 21:03 media
drwxr-xr-x   2 root root 4096 Mar 11 21:03 mnt
drwxr-xr-x   2 root root 4096 Mar 11 21:03 opt
dr-xr-xr-x 125 root root    0 Apr 16 00:10 proc
drwx------   1 root root 4096 Apr 16 01:41 root
drwxr-xr-x   1 root root 4096 Mar 20 19:20 run
drwxr-xr-x   1 root root 4096 Mar 20 19:20 sbin
drwxr-xr-x   2 root root 4096 Mar 11 21:03 srv
dr-xr-xr-x  13 root root    0 Apr 16 00:44 sys
drwxr-xr-x   3 root root 4096 Apr 16 01:30 temp
drwxrwxrwt   2 root root 4096 Mar 11 21:05 tmp
drwxr-xr-x   1 root root 4096 Mar 11 21:03 usr
drwxr-xr-x   1 root root 4096 Mar 11 21:05 var
```
##### Utilizando o link simbolico

```
root@3c435b57cbf2:/# cd dir1

root@3c435b57cbf2:/dir1# pwd
/dir1
```
##### Movendo arquivo ou renomeando
```
mv (move - rename - files)

root@3c435b57cbf2:/home# ls
copiateste2.txt  teste2.txt  workspace

root@3c435b57cbf2:/home# mv teste2.txt workspace/
root@3c435b57cbf2:/home# ls
copiateste2.txt  workspace

root@3c435b57cbf2:/home# cd workspace
root@3c435b57cbf2:/home/workspace# ls
copiateste2.txt  dir1  teste2.txt

root@3c435b57cbf2:/home/workspace# mv -u teste2.txt  testerenomeado.txt
root@3c435b57cbf2:/home/workspace# ls
copiateste2.txt  dir1  testerenomeado.txt
```

##### Manipulacao de arquivo
```
echo 'linux' | cut -c 1-10

root@3c435b57cbf2:/home/workspace# echo 'uma simples string' | cut -c 1-17
uma simples strin
root@3c435b57cbf2:/home/workspace# echo 'uma simples string' | cut -c 1-10
uma simple
root@3c435b57cbf2:/home/workspace# echo 'uma simples string' | cut -c 1-2
um

```
```
grep (print lines mathing a pattern)

root@3c435b57cbf2:/home/workspace# grep -i aliquam testerenomeado.txt
```
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam eget ligula eu lectus lobortis condimentum. **Aliquam** nonummy auctor massa. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.
Nulla at risus. Quisque purus magna, auctor et, sagittis ac, posuere eu, lectus. Nam mattis, felis ut adipiscing
```
##### Contagem
```
```
wc (print newline, word, and byte counts for each file)

root@3c435b57cbf2:/home/workspace# wc testerenomeado.txt
  1  50 344 testerenomeado.txt
```
##### Detalhes do sistema
```
uname (print system information)

root@3c435b57cbf2:/home/workspace# uname -a
Linux 3c435b57cbf2 4.19.76-linuxkit #1 SMP Thu Oct 17 19:31:58 UTC 2019 x86_64 x86_64 x86_64 GNU/Linux
```

##### Mostrando o hostname
```
uname -n

root@3c435b57cbf2:/home/workspace# uname -n
3c435b57cbf2

hostname

root@3c435b57cbf2:/home/workspace# hostname
3c435b57cbf2
```

##### Mostrando há quanto tempo o sistema está rodando.
```
uptime (tell how long the system has been running)

root@3c435b57cbf2:/home/workspace# uptime
 03:09:38 up  7:38,  0 users,  load average: 0.00, 0.00, 0.00
```

##### Mostrando a data e hora atual
```
date (print or set the system date and time)

root@3c435b57cbf2:/home/workspace# date
Thu Apr 16 03:10:57 UTC 2020
```

##### Mostrando calendário (não funciona no Docker)
```
cal (displays a calendar and the date of Easter)

~$ cal
     Abril 2020       
do se te qu qu se sá  
          1  2  3  4  
 5  6  7  8  9 10 11  
12 13 14 15 16 17 18  
19 20 21 22 23 24 25  
26 27 28 29 30   

```
##### rodando multiplos comandos
```
hostname; ls; date

root@3c435b57cbf2:/home/workspace# hostname; ls; date
3c435b57cbf2
copiateste2.txt  dir1  testerenomeado.txt
Thu Apr 16 03:23:04 UTC 2020	 
```



##### Exercitando no server do airflow

##### Checando distribuição do linux server

```
[root@hostname FT_ProspeccaoLeads]# cat /etc/os-release


NAME="CentOS Linux"
VERSION="7 (Core)"
ID="centos"
ID_LIKE="rhel fedora"
VERSION_ID="7"
PRETTY_NAME="CentOS Linux 7 (Core)"
ANSI_COLOR="0;31"
CPE_NAME="cpe:/o:centos:centos:7"
HOME_URL="https://www.centos.org/"
BUG_REPORT_URL="https://bugs.centos.org/"

CENTOS_MANTISBT_PROJECT="CentOS-7"
CENTOS_MANTISBT_PROJECT_VERSION="7"
REDHAT_SUPPORT_PRODUCT="centos"
REDHAT_SUPPORT_PRODUCT_VERSION="7"

```


##### Procurando o arquivo kettle properties a partir do /

```
[root@hostname diegols]# find / -name kettle*

/root/kettle.properties
/root/.kettle/kettle.properties
/home/diegols/kettle.properties


```
##### Encontrando a palavra ncall no arquivo e trazendo 4 linhas antes e depois

```
[root@hostname diegols]# grep -4 ncall /root/kettle.properties

Server Nexcore Postgres
SERVIDOR_PROD_BD_NEXCORE_IP     = 192.168.100.24
SERVIDOR_PROD_BD_NEXCORE_PORTA  = 5432
SERVIDOR_PROD_BD_NEXCORE_NOME   = ncall
SERVIDOR_PROD_BD_NEXCORE_LOGIN  = username_bd
SERVIDOR_PROD_BD_NEXCORE_SENHA
SERVIDOR_PROD_BD
```


##### Qual o diretorio estou
```
[root@hostname FT_ProspeccaoLeads]# pwd

/work/prb/logs/dw_transformations/Fato/FT_ProspeccaoLeads

```

##### Listando arquivos que contenham 202004
```
[root@hostname FT_ProspeccaoLeads]# ls -ltrh *202004*

-rw-r--r--. 1 root root 19K Apr  1 06:14 FT_ProspeccaoLeads202004010555.log
-rw-r--r--. 1 root root 19K Apr  2 15:22 FT_ProspeccaoLeads202004021456.log
-rw-r--r--. 1 root root 19K Apr  3 09:47 FT_ProspeccaoLeads202004030914.log
-rw-r--r--. 1 root root 19K Apr  4 09:35 FT_ProspeccaoLeads202004040922.log
-rw-r--r--. 1 root root 19K Apr  5 06:48 FT_ProspeccaoLeads202004050636.log
-rw-r--r--. 1 root root 19K Apr  6 06:56 FT_ProspeccaoLeads202004060635.log
-rw-r--r--. 1 root root 19K Apr  7 08:23 FT_ProspeccaoLeads202004070808.log
-rw-r--r--. 1 root root 19K Apr  8 06:36 FT_ProspeccaoLeads202004080620.log
-rw-r--r--. 1 root root 19K Apr  9 08:08 FT_ProspeccaoLeads202004090751.log
[root@hostname FT_ProspeccaoLeads]#
```


##### Listando as primeiras linhas com head

```
[root@hostname FT_ProspeccaoLeads]# head 202004090751.log

#######################################################################
WARNING:  no libwebkitgtk-1.0 detected, some features will be unavailable
    Consider installing the package with apt-get or yum.
    e.g. 'sudo apt-get install libwebkitgtk-1.0-0'
#######################################################################
Java HotSpot(TM) 64-Bit Server VM warning: ignoring option MaxPermSize=1024m; support was removed in 8.0
log4j:WARN Continuable parsing error 45 and column 76
log4j:WARN Element type "rollingPolicy" must be declared.
log4j:WARN Continuable parsing error 52 and column 14
log4j:WARN The content of element type "appender" must match "(errorHandler?,param*,layout?,filter*,appender-ref*)".
[root@hostname FT_ProspeccaoLeads]#
```

#####Listando as ultimas 10 linhas com tail (tail -f *)

```
[root@hostname FT_ProspeccaoLeads]# tail -10 202004090751.log

2020/04/09 08:08:47 - FT_ProspeccaoLeads - Transformation lines written: 13623 ( 908 lines/s)
2020/04/09 08:08:47 - FT_ProspeccaoLeads - Starting entry [Success]
2020/04/09 08:08:47 - FT_ProspeccaoLeads - Finished job entry [Success] (result=[true])
2020/04/09 08:08:47 - FT_ProspeccaoLeads - Finished job entry [FT_ProspeccaoLeads_RetornoMidia] (result=[true])
2020/04/09 08:08:47 - FT_ProspeccaoLeads - Finished job entry [FT_ProspeccaoLeads_FaceSite] (result=[true])
2020/04/09 08:08:47 - FT_ProspeccaoLeads - Finished job entry [FT_ProspeccaoLeads] (result=[true])
2020/04/09 08:08:47 - FT_ProspeccaoLeads - Job execution finished
2020/04/09 08:08:47 - Kitchen - Finished!
2020/04/09 08:08:47 - Kitchen - Start=2020/04/09 07:51:38.829, Stop=2020/04/09 08:08:47.639
2020/04/09 08:08:47 - Kitchen - Processing ended after 17 minutes and 8 seconds (1028 seconds total).
[root@hostname ]#
```

##### Qual user estou logado
```
[diegols@hostname ~]$ whoami
diegols
```

##### Verificando o conteudo do arquivo com o cat

```
[root@hostname diegols]# cat /root/kettle.properties


# This file was generated by Pentaho Data Integration version 8.2.0.0-342.
#
# Here are a few examples of variables to set:
#
# PRODUCTION_SERVER = hercules
# TEST_SERVER = zeus
# DEVELOPMENT_SERVER = thor
#
# Note: lines like these with a # in front of it are comments
#
KETTLE_SYSTEM_HOSTNAME = 127.0.0.1

##PRB PATH
PRB_PATH=/work/pentaho/dw_transformations/
```

##### Listando o tamanho dos mounts
```
[diegols@hostname ~]$ df -h
Filesystem                    Size  Used Avail Use% Mounted on
devtmpfs                       63G     0   63G   0% /dev
tmpfs                          63G     0   63G   0% /dev/shm
tmpfs                          63G  234M   63G   1% /run
tmpfs                          63G     0   63G   0% /sys/fs/cgroup
/dev/mapper/rootvg-rootlv     976M  157M  753M  18% /
/dev/mapper/rootvg-usrlv      3.9G  3.3G  317M  92% /usr
/dev/sda1                     976M  271M  639M  30% /boot
/dev/mapper/rootvg-tmplv      976M  328M  582M  37% /tmp
/dev/mapper/rootvg-optlv      976M  476M  434M  53% /opt
/dev/mapper/rootvg-homelv     2.0G   60M  1.8G   4% /home
/dev/mapper/rootvg-varlv      2.0G  690M  1.2G  38% /var
/dev/mapper/appvg-wloglv      118G   91G   22G  81% /work/prb
/dev/mapper/appvg-wpentaholv   99G  7.2G   87G   8% /work/pentaho
tmpfs                          13G     0   13G   0% /run/user/0
tmpfs                          13G     0   13G   0% /run/user/1005
```

##### Listando as 10 maiores pastas
```
[root@hostname diegols]# du -a /var | sort -n -r | head -n 10
699748  /var
472868  /var/cache
470468  /var/cache/yum
470464  /var/cache/yum/x86_64
470460  /var/cache/yum/x86_64/7
279992  /var/cache/yum/x86_64/7/REPOSITORIO-LOCAL
237888  /var/cache/yum/x86_64/7/REPOSITORIO-LOCAL/gen
237884  /var/cache/yum/x86_64/7/REPOSITORIO-LOCAL/gen/primary_db.sqlite
176876  /var/lib
153892  /var/lib/rpm
[root@hostname diegols]#
```
##### Checando quantidade de memoria em gigabytes
```

[root@hostname diegols]# free -g
              total        used        free      shared  buff/cache   available
Mem:            125           2          90           0          32         121
Swap:             1           0           1
```

##### Checando quantidade de memoria em megabytes
```
[root@hostname diegols]# free -m
              total        used        free      shared  buff/cache   available
Mem:         128771        2950       92107         363       33712      124849
Swap:          2047          29        2018
[root@hostname diegols]#
```
##### Usando o VI
(VICheatsheet)[http://www.atmos.albany.edu/daes/atmclasses/atm350/vi_cheat_sheet.pdf]




