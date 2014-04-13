JDK
---

Vamos usar o _Java SE Development Kit 6 Update 35_, 
é a mais atual até o momento que escrevo esta documentação. Não vamos obter o arquivo rpm, mas o binário simples.


### Faça o download no site da Oracle:                
[http://www.oracle.com/technetwork/java/javase/downloads/jdk6u35-downloads-1836443.html](http://www.oracle.com/technetwork/java/javase/downloads/jdk6u35-downloads-1836443.html)
    

### Execute 

    # chmod 777 jdk-6u35-linux-x64.bin
    ./jdk-6u35-linux-x64.bin

Repare que instalei o arquivo binário como usuário normal. Agora faça uma cópia do diretório que acabou de ser criado para `/usr/java`: 

    # cp /jdk1.6.0_35 /usr/java
