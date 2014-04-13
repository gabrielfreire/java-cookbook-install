Tomcat 7
---

Baixe a última versão:           
[http://tomcat.apache.org/download-70.cgi](http://tomcat.apache.org/download-70.cgi)

Depois de realizar o donwload do arquivo, copie-o para a pasta /usr/java e, utilizando
o comando tar, extraia o arquivo nesse diretório, conforme a seguir.

    tar xvfz apache-tomcat-7.0.53


Copie a pasta com o conteúdo da instalação

    # cp /apache-tomcat-7.0.53 /usr/java


Vamos definir a variável de ambiente CATALINA_HOME. Edite novamente o arquivo `/etc/profile`
e adicione a seguinte linha no final do arquivo:

    export CATALINA_HOME=/usr/java/apache-tomcat-7.0.53


Para iniciar o Apache Tomcat 7 execute a partir de `CATALINA_HOME\bin`:

    sh startup.sh


Para finalizar o Apache Tomcat 7...

    sh shutdown.sh


### Teste de instalação

Depois de iniciar o Apache Tomcat, abra o navegador e digite:

    http://localhost:8080
    

Deverá aparecer uma página com as informações sobre o Apache Tomcat.


### Portas

Por padrão, o Tomcat vem com a porta 8080, veja a seguir quais são as portas padrão
do Tomcat.

    8080 - Serviço de HTTP
    8005 - Serviço de shutdown
    8009 - Conector AJP/1.3
    8443 - Porta de HTTPS


Se você estiver tendo problemas com a numeração de portas é se a página principal
`http://localhost:8080` não abre. Isso geralmente é um conflito com outra
porta em funcionamento no seu servidor.
Se quiser confirmar o problema, entre no arquivo de log localizado em `CATALINA_HOME\logs`.

Para substituir essas portas, altere o arquivo `CATALINA_HOME\conf\server.xml`.