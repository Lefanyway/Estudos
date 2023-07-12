# Guia completo do Linux
>  Esse repositório tem como objetivo guardar todas as minhas anotações com base nos meus estudos de Linux;
 ***
# Explicando o terminal

### `Lefanyway@servidor01:~$`

`Lefanyway`= Nome de usuário usando o terminal;

`servidor01`= Nome da máquina;

`:`= Separador;

`~` = Simboliza o diretório Home, onde está a pasta do usuário;

`/`= Simboliza o diretório raiz onde está todos as pastas e arquivos;

`$`= Identifica quando o usuário é um USER padrão (sem permissões privilegiadas)

`#` = Identifica quando o usuário é ROOT; (ROOT é o usuário privilegiado capaz de executar comandos sensíveis, Você pode tudo!)

***
# Comandos de atalho

Sair do modo root CTRL+D

CTRL+A para mover o cursor para o inicio da linha de comandos.

CTRL+E para mover o cursor para o fim da linha de comandos.

CTRL+U para apagar o que estiver à esquerda do cursor. 

CTRL+K para apagar o que estiver à direita do cursor. 


***
## Estrutura de diretórios
/bin - Binários de usuários, comandos e executavéis;

/boot - Arquivos essenciais para a inicialização do sistema;

/dev - Dispositivos do sistema;

/sbin - Binários do superusuário, essenciais no boot;

/etc - Arquivos de configuração globais;

/run - contém informações de serviços;

/home - Armazenamento de dados de contas de usuários;

/lib - bibliotecas de sistema e módulos do kernel;

/media - ponto de montagem de dispositivos

/mnt - ponto de montagem temporário;

/proc - diretório que tem informações do sistema, incluindo os processos, memória, dispositivos.;

/root - diretório home exclusivo do root;

/sys - arquivos de sistema;

/usr - armazena todas as aplicações e programas que são instalados depois da configuração inicial do sistema operacional;

/var - Uns dos mais importantes, contém arquivos de variáveis que mudarão conforme o sistema operacional está sendo usado, coisas como logs, arquivos cache e temporários;


***
# Comandos básicos
<p> `ip addr show`= mostrar interfaces de rede, ip <p>
`reboot` = comando para reiniciar o sistema operacional;
`clear` = limpa o terminal;
`su -`= Comando para mudar de usuário;
`sudo su`= Comando para mudar para root;
`cd` = comando para mudar de Diretório;
`cd -` = voltar para o caminho de diretórios anteriores;
`ls -l` = Listar os arquivos da pasta corrente mostrando mais detalhadamente o tamanho dos arquivos, permissões etc;
`mkdir` = cria um diretório;
`rmdir` = remove um diretório;
`cp` = copia um contéudo;
`mv` = possibilita renomear e mover arquivos;
`pwd` = imprime o diretório que você ta atualmente;
`touch` = cria um arquivo em branco;
`date` = imprime dia e hora; 
`df -h` = mostra informações de partições mais especificados;
`du -sh` = mostra o tamanho do diretório
`free` = mostra informações da memória
`sort` = lista os arquivos de ordem alfabética;
`cat` = para visualizar o contéudo de um arquivo, com shift + pgup/pgdown subir e descer o texto;
`tail` = imprime o "rabo" do contéudo (ultimas linhas do contéudo); 
`head` = imprime a "cabeça" do contéudo (header do contéudo);
`which ls` = imprime onde certo comando se encontra (no caso, a raiz do `ls`)  
`find /etc -name n*` = procura no diretório /etc  nome de algum arquivo ou diretório que contém o "n", e o asterisco completa as letras que falta;
`cut` separa campos de informações
`less` = Possibilita ler arquivos grande e tem a função de descer e subir no arquivo, e para pesquisar algum arquivo no arquivo basta usar: "/arquivo que deseja";
`grep` = comando para filtrar informações de um determinado arquivo;
`echo` = imprime uma mensagem na tela;
`chattr` = troca o atributo;
`apt-get` = é um gerenciador de pacotes que permite baixar, remover e atualizar aplicativos

***
# Administração de usuários

`adduser` = Adicionar usuário
`useradd` = Adicionar usuário, porém através de parametros
`userdel` = remover usuário
`addgroup` = criar grupo
`groupadd` = criar grupo, porém através de parametros
`groupdel` = deletar grupo
`passwd` = configurações de senha de usuário 
`passwd -de "usuario"` = quando esquecer a senha do usuário;
`gpasswd` = configurações de senha de grupos, adiciona usuários e seta um administrador.
`newgrp` = participar de uma um grupo durante uma sessão
`usermod` = modificar configurações usuários
`groupmod` = modificar configurações de grupos 
`last` = mostra informações de logins 
`lastlog` = mostra os ultimos usuários que logaram

***

# Permissões

`chmod` = modifica as permissões
`chown` = modifica o dono, grupo e diretório do arquivo
`chgrp` = modifica o grupo dono do arquivo
`umask` = define a permissão padrão do arquivo




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

`tar cpvf arquivo.tar /pasta` = para compactar arquivos em uma "pasta"
`tar -xzf projetos.tar.gz` = para descompactar


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
`G` = vai para a ultima linh
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

### sintaxe if
if [ ]; then
  echo "?"
fi

### sintaxe for
for i in $(seq 1 10); do
  if [ i == "5" ]; then
    echo "Número $i"
  fi
done

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


