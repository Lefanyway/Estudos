
# Guia completo do Linux

> Esse repositório tem como objetivo guardar todas as minhas anotações com base nos meus estudos de Linux, Se estiver algo errado me perdoe ;) </p>

***

# Explicando o terminal

<p>`Lefanyway@servidor01:~$`</p>

<p>`Lefanyway`= Nome de usuário usando o terminal; <b></p>

<p>`servidor01`= Nome da máquina;<b></p>

<p>`:`= Separador;<b></p>

<p>`~` = Simboliza o diretório Home, onde está a pasta do usuário;<b></p>

<p>`/`= Simboliza o diretório raiz onde está todos as pastas e arquivos;<b></p>

<p>`$`= Identifica quando o usuário é um USER padrão (sem permissões privilegiadas)<b></p>

<p>`#` = Identifica quando o usuário é ROOT; (ROOT é o usuário privilegiado capaz de executar comandos sensíveis, Você pode tudo!)<b></p>

***

# Comandos de atalho

<p>Sair do modo root CTRL+D<b></p>

<p>CTRL+A para mover o cursor para o inicio da linha de comandos.<b></p>

<p>CTRL+E para mover o cursor para o fim da linha de comandos.<b></p>

<p>CTRL+U para apagar o que estiver à esquerda do cursor. <b></p>

<p>CTRL+K para apagar o que estiver à direita do cursor. <b></p>

***

## Estrutura de diretórios

<p>/bin - Binários de usuários, comandos e executavéis;<b></p>

<p>/boot - Arquivos essenciais para a inicialização do sistema;<b></p>

<p>/dev - Dispositivos do sistema;<b></p>

<p>/sbin - Binários do superusuário, essenciais no boot;<b></p>

<p>/etc - Arquivos de configuração globais;<b></p>

<p>/run - contém informações de serviços;<b></p>

<p>/home - Armazenamento de dados de contas de usuários;<b></p>

<p>/lib - bibliotecas de sistema e módulos do kernel;<b></p>

<p>/media - ponto de montagem de dispositivos<b></p>

<p>/mnt - ponto de montagem temporário;<b></p>

<p>/proc - diretório que tem informações do sistema, incluindo os processos, memória, dispositivos.;<b></p>

<p>/root - diretório home exclusivo do root;<b></p>

<p>/sys - arquivos de sistema;<b></p>

<p>/usr - armazena todas as aplicações e programas que são instalados depois da configuração inicial do sistema operacional;<b></p>

<p>/var - Uns dos mais importantes, contém arquivos de variáveis que mudarão conforme o sistema operacional está sendo usado, coisas como logs, arquivos cache e temporários;<b></p>


***

# Comandos básicos

<p>`ip addr show`= mostrar interfaces de rede, ip <b></p>
 
<p>`ping` = envia pacotes até um ip para ver se há conexão entre eles<b></p>

<p>`traceroute` = mostra a rota de pacotes enviado desde o seu ip até o destino<b></p>

<p>`netcat/nc` = ele possibilita se conectar em uma porta aberta<b></p>

<p>`reboot` = comando para reiniciar o sistema operacional;<b></p>

<p>`clear` = limpa o terminal;<b></p>

<p>`su -`= Comando para mudar de usuário;<b></p>

<p>`sudo su`= Comando para mudar para root;<b></p>

<p>`cd` = comando para mudar de Diretório;<b></p>

<p>`cd -` = voltar para o caminho de diretórios anteriores;<b></p>

<p>`ls -l` = Listar os arquivos da pasta corrente mostrando mais detalhadamente o tamanho dos arquivos, permissões etc;<b></p>

<p>`mkdir` = cria um diretório;<b></p>

<p>`rmdir` = remove um diretório;<b></p>

<p>`cp` = copia um contéudo;<b></p>

<p>`mv` = possibilita renomear e mover arquivos;<b></p>

<p>`pwd` = imprime o diretório que você ta atualmente;<b></p>

<p>`touch` = cria um arquivo em branco;<b></p>

<p>`date` = imprime dia e hora; <b></p>

<p>`df -h` = mostra informações de partições mais especificados;<b></p>

<p>`du -sh` = mostra o tamanho do diretório<b></p>

<p>`free` = mostra informações da memória<b></p>

<p>`sort` = lista os arquivos de ordem alfabética;<b></p>

<p>`cat` = para visualizar o contéudo de um arquivo, com shift + pgup/pgdown subir e descer o texto;<b></p>

<p>`tail` = imprime o "rabo" do contéudo (ultimas linhas do contéudo); <b></p>

<p>`head` = imprime a "cabeça" do contéudo (header do contéudo);</p>

<p>`which ls` = imprime onde certo comando se encontra (no caso, a raiz do ls)</p>

<p>`find /etc -name n*` = procura no diretório /etc  nome de algum arquivo ou diretório que contém o "n", e o asterisco completa as letras que falta;</p>

<p>`cut` separa campos de informações</p>

<p>`less` = Possibilita ler arquivos grande e tem a função de descer e subir no arquivo, e para pesquisar algum arquivo no arquivo basta usar: "/arquivo que deseja";</p>

<p>`grep` = comando para filtrar informações de um determinado arquivo;</p>

<p>`echo` = imprime uma mensagem na tela;</p>

<p>`chattr` = troca o atributo;</p>

<p>`apt-get` = é um gerenciador de pacotes que permite baixar, remover e atualizar aplicativos</p>

***

# Administração de usuários

<p>`adduser` = Adicionar usuário</p>

<p>`useradd` = Adicionar usuário, porém através de parametros</p>

<p>`userdel` = remover usuário</p>

<p>`addgroup` = criar grupo</p>

<p>`groupadd` = criar grupo, porém através de parametros</p>

<p>`groupdel` = deletar grupo</p>

<p>`passwd` = configurações de senha de usuário </p>

<p>`passwd -de "usuario"` = quando esquecer a senha do usuário;</p>

<p>`gpasswd` = configurações de senha de grupos, adiciona usuários e seta um administrador.</p>

<p>`newgrp` = participar de uma um grupo durante uma sessão</p>

<p>`usermod` = modificar configurações usuários</p>

<p>`groupmod` = modificar configurações de grupos </p>

<p>`last` = mostra informações de logins </p>

<p>`lastlog` = mostra os ultimos usuários que logaram</p>

***

# Permissões

<p>`chmod` = modifica as permissões</p>

<p>`chown` = modifica o dono, grupo e diretório do arquivo</p>

<p>`chgrp` = modifica o grupo dono do arquivo</p>

<p>`umask` = define a permissão padrão do arquivo</p>

## Representação de permissões
## | - | rw- | rw- | r--| 

### Letra
`r`= permissão de read (leitura)

`w` = permissão de write (escrita) 

`x` = permissão execução 

`-` = ausência da permissão

### octal 
`r` = 4

`w` = 2

`x` = 1

`-` = 0
### Simbólico
`u` = dono

`g` = grupo dono

`o` = outros

`a` = all
### atribuicão de permissões
`+` = adiciona permissão

`-` = remove permissão

`=` = deixa todos iguais


`rwx` = 777
## Primeira coluna | - |
`-` = arquivo de texto

`d` = diretório 

`l` = link simbólico


## Segunda coluna | rw- |
permissões do dono do arquivo

O dono do arquivo tem permissões de `r = (leitura)` e `w`= (escrita)

## Terceira coluna | rw- |
dono do grupo tem permissão de `r = (leitura)` e `w = (escrita)`

## Quarta coluna | r-- |
 outros, todos que não são dono e nem faz parte do grupo tem permissão de  `r = (leitura)` apenas

***

## Compactando e descompactando

<p>`tar cpvf arquivo.tar /pasta` = para compactar arquivos em uma "pasta"</p>

<p>`tar -xzf projetos.tar.gz` = para descompactar</p>


***
# VIM
`ESC` =  retorna ao modo comando
## Modo de inserção
`i` = inserir texto

`I` = inserir no inicio da linha

`o` = inserir na linha de baixo

`O` = inserir na linha de cima

`a` = inserir um caractere a frente

`A` = inserir no final  da linha

`b`= pula palavra por palavra para trás

`w` = pula palavra por palavra frente

`SHIFT + $` = pula para o final da linha
## Salvando e saindo
`:w` = salvar

`:q` = sair/quit

`:q!` = sair forçadamente

`:wq` = salvando e saindo

`:x` = salvando e saindo

`ZZ` = zair e zalvar

`ZQ` = zair e não salvar
## Copiando, colando e recortando
`yy` = copiar

`p` = colar na linha de baixo

`P`= cola na linha de cima

`y8y` = copiar 8 linhas (yNy - copiar N linhas) 

`dd` = apaga o recorta a linha inteira

`dw` = apaga uma palavra

`cw` = recorta uma palavra

`yw` = copiar uma palavra

`d8d` = apaga/recorta 8 linhas (dNd - apaga/recorta N linhas) 

`x` = apaga caractere igual ao delete

`X` = apaga caractere antes do cursor igual ao backspace

`r + N` = replace - substituir o caractere atual pelo N

## Visual
`v` = selecionar um pedaço do texto

`CTRL + v` = selecionar um bloco de texto
## Voltando e refazendo
`u` = voltar 
`CTRL + R` = refazer



## Buscas e localização
`/neymar` = buscar a palavra neymar descendo o arquivo

`?neymar` = buscar a palavra neymar subindo o arquivo

`n` = continua com a busca indo para baixo

`N` = continua a busca indo para cima

`gg` = vai para a primeira linha

`G` = vai para a ultima linha

`M` = meio da tela

`H` = em cima da tela

`L` = embaixo da tela


***
# Variáveis de ambiente
`echo $PATH` = Visualizar a variavel de ambiente

`printenv PATH` = visualizar a variavel de ambiente

`export VAR="value"` = setar variavel de ambiente

`unset VAR` = deletar variavel

`alias ls='ls -lha'` = irá criar um atalho/apelido para o ls

`/etc/environment` = arquivo para armazenar as variáveis


***

# ShellScript
#!/bin/bash = especificando o interpretador de comandos

`#` = comentário

exit code 0 = programa executado corretamente, sem erros.

exit code 1 = programa executou com erros 

exit code 2 = programa indicou erros de sintaxe.

***
# Comandos Coringas

`*` = exemplo de comando: `ls a*` vai listar tudo que começa com a letra "a". é possível procurar só com os caracteres finais, por exemplo: `ls *m` vai listar tudo que termina com a letra "m".

`?` = é usado para completar o nome do arquivo que você não saiba a letra;




***
## Alguns comandos que pode te ajudar
`man ls` = mostra o manual de como usar o `ls`

`ls --help` = mostra alguns paramêtros que pode ser usado com `ls`

`cat /etc/os-release` = para ver informações da distro

`whoami` = mostra quem é você no terminal

