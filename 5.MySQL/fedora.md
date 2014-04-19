MySQL
---

Faça o download:       
[http://dev.mysql.com/downloads/mysql/](http://dev.mysql.com/downloads/mysql/)

O pacote de download é __Linux - Generic (glibc 2.5) (x86, 64-bit), Compressed TAR Archive__,
no qual o nome do arquivo é mysql-5.6.17-linux-glibc2.5-x86_64.tar.gz.

Tome cuidado ao fazer o download, existem diversos pacotes disponíveis, mudando somente
o nome do arquivo no site.

### Execute

    # groupadd mysql
    # useradd -g mysql mysql
    # cd /usr/local
    # tar zxvf caminho/do/arquivo/mysql-<versão>-<so>.tar.gz
    # ln -s /mysql-<versão>-<so> mysql
    # cd mysql
    # chown -R mysql .
    # chgrp -R mysql .
    # scripts/mysql_install_db --user=mysql
    # chown -R root .
    # chown -R mysql data


_Iniciar o MySQL_

    # bin/mysqld_safe --user=mysql &

_Finalizar o MySQL_

    # bin/mysqladmin -u root -p shutdown

_Alterar senha_

    # bin/mysqladmin -u root password nova_senha


Para incluir os executáveis no PATH, acrescente no arquivo `/etc/profile` a seguinte linha:

    export PATH=$PATH:/usr/local/mysql/bin


Faça uma cópia do executável para iniciar o mysql facilmente:

    # cp /usr/local/mysql/support-files/mysql.server /etc/init.d/mysqld


Para iniciar o serviço, agora você pode executar:

    # /etc/init.d/mysqld start


### Erros

Devemos tomar cuidado no caso de existir outro arquivos do mysql no servidor, caso já tenha sido instalado
ou está instalado atualmente. Principalmente se foi via _yum_, pois não ficará em um único diretório.

O mais comum são diretórios `mysql/` e o arquivo `etc/my.cnf`. A seguir um erro causado pela existência deste arquivo:

    Starting MySQL... ERROR! The server quit without updating PID file (/var/lib/my                         sql/server.pelayan.com.pid).

Em nossa instalação que está concentrada no diretório `/usr/local/mysql`, já foi criado um arquivo de mesmo nome, temos que impedir que o arquivo em questão seja lido ao executar o mysql, execute:

    # mv /etc/my.cnf /etc/my.cnf.old
    
