Eclipse
---

Faça o download:       
[http://www.eclipse.org/downloads/](http://www.eclipse.org/downloads/)


Em nosso caso, a melhor opção é a __Eclipse IDE for Java EE Developers__.
Depois de realizar o download do arquivo, copie-o para a pasta `/usr/java`.

Execute o comando _tar_ para extrair o arquivo nesse diretório:

    tar xvfz eclipse-jee-galileo-SR2-linux-gtk-x86_64.tar.gz

Depois de extraído, entre na pasta `eclipse/` e execute:

    ./eclipse


### Criar atalho

No fedora, a forma mais prática é criar um atalho manualmente, execute:

    # nano /usr/share/applications/eclipse.desktop


Agora, adicione as seguintes linhas no arquivo:

    [Desktop Entry]
    Name=Eclipse
    Comment=IDE de programação
    Exec=/usr/java/eclipse/eclipse
    Icon=/usr/java/eclipse/icon.xpm
    Categories=GTK;Development;IDE;
    Type=Application


Pronto, agora o Eclipse está visível no menu de aplicativos. Para torná-lo um favorito,
clique com o botão direito sobre ele e selecione _Adicionar aos favoritos_.


