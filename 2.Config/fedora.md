Configurar java 1.7
---

Para configurar o java, edite o arquivo `/etc/profile` e adicione as novas 
variáveis de ambiente com o seguinte conteúdo ao final do arquivo:

    export JAVA_HOME=/usr/java/jdk1.6.0_35                                                                            
    export CLASSPATH=.:$CLASSPATH                                                                                     
    export PATH=$JAVA_HOME/bin:$PATH  

Depois de salvar, digite _java -version_ para testar o funcionamento do java,
o resultado deverá ser semelhante ao exemplo a seguir:

    java version "1.7.0_51"                                                                                           
    OpenJDK Runtime Environment (fedora-2.4.5.1.fc20-x86_64 u51-b31)                                                  
    OpenJDK 64-Bit Server VM (build 24.51-b03, mixed mode) 

_Obs: Se não exibir um conteúdo semelhante a esse, reinicie o SO para reforçar a aceitação
das novas variáveis de ambiente._
