--> CRIANDO CHAVE SSH NO SEU PC LOCAL <--

* Abra seu GIT BASH e siga a sequência dos comandos e o que eles pedem

1. Criando Chave SSH na sua máquina local

    <code> ssh-keygen -t ed25519 -C "Digite seu email aqui" </code>

    Vai retornar essas duas mensagens:

    <em style='color: greenyellow'> -> Generating public/private ed25519 key pair. / Gerando par de chaves ed25519 pública/privada. </em>


    <em style='color: greenyellow'> ->Enter file in which to save the key (/c/Users/herms/.ssh/id_ed25519): / Insira o arquivo no qual deseja salvar a chave (/c/Users/herms/.ssh/id_ed25519):</em>

    Na primeira mensagem nos informa que nossa chave pública e privada foi gerada
    <br>
    Já na segunda nos retorna uma pergunta em qual diretório desejamos salvar as chaves

    Por padrão vamos dar um ENTER e irá salvar na nossa pasta (/c/Users/herms/.ssh/id_ed25519) e retornar:

    <em style='color: greenyellow'>Created directory '/c/Users/herme/.ssh'.</em>

    Agora irá pedir uma senha:

    <em style='color: greenyellow'>Enter passphrase (empty for no passphrase):</em>

    Por padrão pode pressionar ENTER

    <em style='color: greenyellow'>Enter same passphrase again:</em>

    Por padrão pode pressionar ENTER

    Caso tudo ocorra certo, irá retornar as seguintes mensagens:

    <em style='color: greenyellow'>
    Your identification has been saved in /c/Users/herme/.ssh/id_ed25519
    <br>
    Your public key has been saved in /c/Users/herme/.ssh/id_ed25519.pub
    </em>
    <br>
    <br>
    <em style='color: greenyellow'>The key fingerprint is:</em>

    <em style='color: greenyellow'>
    SHA256:OX5qdGYwe55muEwx5U8txCB/nrpKMM5R9o3WOeXSRys hermerson_landim@hotmail.com
    <br>
    The key's randomart image is:
    <br>
    +--[ED25519 256]--+<br>
    |        . .      |<br>
    |         o o     |<br>
    |        o o + . .|<br>
    |       oo= B B ..|<br>
    |      + S+= @E+..|<br>
    |     o =o==+ +.. |<br>
    |      o.+Bo..    |<br>
    |       +oo=.     |<br>
    |       .==.      |<br>
    +----[SHA256]-----+<br>
    </em>
    <br>
    Ok, agora temos nossa chave SSH pública e privada instaladas, agora precisamos adicionar
    <br>
    nossa chave SSH ao ssh-agent para podermos gerenciar nossas chaves.
    <br>
    <br>
2. Adicionando a chave SSH ao ssh-agent
    <br>
    <!-- Caso você tenha instalado outras chaves SSH na sua máquina siga esses passos:
    <br>
    1. Verifique se existem chaves SSH existentes digitando o seguinte comando:
    <br> -->
    Digite o seguinte código no seu git-bash:
    <br>
    <code>eval "$(ssh-agent -s)"</code>
    <br>
    <br>
    No fluxo normal, irá nos retornar a seguinte mensagem:
    <br>
    <em style='color: greenyellow'>Agent pid 'algum número'</em>
    <br>
    <br>
    Seguindo nosso fluxo, vamos adicionar o seguinte comando para padronizar
    <br>
    o nome da nossa chave SSH:
    <br>
    <br>
    <code>ssh-add ~/.ssh/id_ed25519</code>
    <br>
    <br>
    Novamente, seguindo nosso fluxo normal, retornará a seguinte mensagem de sucesso:
    <br>
    <em style='color: greenyellow'>Identity added: /c/Users/herme/.ssh/id_ed25519 (hermerson_landim@hotmail.com)</em>
    <br>
    <br>
    Pronto, nossa chave SSH já está criada e adicionado ao nosso ssh-agent!
    <br>
    Agora o próximo passo é adiciona-la no seu seu gitHub.

3. Adicionando chave SSH ao gitHub

    <br>
    <br>
    Primeiro de tudo copie sua chave SSH usando o seguinte comando no seu gitBash:
    <br>
    <br>
    <code>clip < ~/.ssh/id_ed25519.pub</code>
    <br>
    Por padrão não retornará nenhuma mensagem.
    <br>
    <br>
    Agora vá ao seu gitHub > Settings(Configurações) > SSH and GPG Keys
    <br>
    Clique em New SSH key (Nova chave SSH)
    <br>
    <br>
    Defina um título a sua escolha e cole a chave SSH no campo Key e clique em add SSH key
    <br>
    Insira sua senha e prontinho!
    <br>
    Agora você pode clonar e subir seus projetos do gitHub pra sua máquina local.
    <br>
    Tenha bom proveito!
    <br>
    <br>
    <code>Créditos: Hérmerson Landim</code>








