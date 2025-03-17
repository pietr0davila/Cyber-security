
ls -l
O comando ls -l faz parte de ls mas é mais avançado, ele exibe informações avançadas do diretório especificado

```
total 32
drwxr-xr-x 2 cry0l1t3 htbacademy 4096 Nov 13 17:37 Desktop
drwxr-xr-x 2 cry0l1t3 htbacademy 4096 Nov 13 17:34 Documents
drwxr-xr-x 3 cry0l1t3 htbacademy 4096 Nov 15 03:26 Downloads
drwxr-xr-x 2 cry0l1t3 htbacademy 4096 Nov 13 17:34 Music
drwxr-xr-x 2 cry0l1t3 htbacademy 4096 Nov 13 17:34 Pictures
drwxr-xr-x 2 cry0l1t3 htbacademy 4096 Nov 13 17:34 Public
drwxr-xr-x 2 cry0l1t3 htbacademy 4096 Nov 13 17:34 Templates
drwxr-xr-x 2 cry0l1t3 htbacademy 4096 Nov 13 17:34 Videos
```
total 32 - tamanho total em bits (1 bit = 1024byte)
drwxr-xr-x - tipo e pemissões
2 - links internos no diretório
cry0l1t3 - dono do diretório
htbacademy - grupo dono do diretório
4096 - tamanho ou número de blocos alocados na memória
Nov 13... - data atual
Desktop - nome do diretório

arquivos ocultos tem . antes do nome, ls por padrão não mostra diretórios, ocultos, só mostra com a flag -la
drwxr-xr-x 2 cry0l1t3 htbacademy 4096 Nov 13 17:37 .bash_history

o comando touch cria um arquivo
`touch arquivo`

mkdir cria um diretório
`mkdir diretório`

Para criar um diretório pai (diretório com outros diretórios dentro) podemos usar a flag -p

O comando `tree .` te mostra a arvore de todo o sistema no diretório atual

```
anotherMan@htb[/htb]$ tree .

.
├── info.txt
└── Storage
    └── local
        └── user
            ├── documents
            └── userinfo.txt

4 directories, 2 files
```

O comando mv (q move arquivos) pode ser usado para renomear caso o 2° parâmetro seja um nome de um arquivo ao invés de diretório

A edição de arquivos pode ser feita a partir do nano, vim ou vi. o nano é menos usado porém mais simples

`nano notes.txt`

abre o arquivo notes.txt (se não existir cria) e permite que você edite o texto nele

```
  GNU nano 2.9.3                                    notes.txt                                              

Here we can type everything we want and make our notes.▓


^G Get Help    ^O Write Out   ^W Where Is    ^K Cut Text    ^J Justify     ^C Cur Pos     M-U Undo
^X Exit        ^R Read File   ^\ Replace     ^U Uncut Text  ^T To Spell    ^_ Go To Line  M-E Redo
```
^ equivale ao nosso ctrl, ctrl+O salva o arquivo e ctrl+W procura por uma palavra no arquivo

Para abrir o arquivo saímos do nano com ctrl+X e usamo `cat notes.txt` para ler o conteúdo. Existem arquivos importantes mal configurados que podem garantir acesso ao sistema administrativo, /etc/passwd é um exemplo, contém informações do sistema como usuários, UIDs (user ID), GIDs (group ID). Antigamente armazenava senhas, mas elas foram alteradas para um arquivo mais rigido /etc/shadow. De qualque forma, o passwd mal configurado pode permiter a escalada de privilégios ou  expor dados importantes

Vim
Editor de texto ASCII (Assim como o nano) e é uma versão melhorada do vi. Ele fornece interface para comandos externos como grep para pesquisa

```
  1 $
~
~                              VIM - Vi IMproved                                
~                                                                               
~                               version 8.0.1453                                
~                           by Bram Moolenaar et al.                            
~           Modified by pkg-vim-maintainers@lists.alioth.debian.org             
~                 Vim is open source and freely distributable                   
~                                                                               
~                           Sponsor Vim development!                            
~                type  :help sponsor<Enter>    for information                  
~                                                                               
~                type  :q<Enter>               to exit                          
~                type  :help<Enter>  or  <F1>  for on-line help                 
~                type  :help version8<Enter>   for version info                 
~                                                                           
```
Vim diferencia entre texto e entrada de comando e oferece 6 modos 

| Mode          | Descrição                                                                 |
|---------------|--------------------------------------------------------------------------|
| Normal        | Modo padrão ao abrir o Vim, usado para navegação e comandos               |
| Insert        | Modo de inserção de texto, ativado com `i`, `I`, `a`, `A`, `o`, `O`       |
| Visual        | Modo de seleção de texto, ativado com `v`, `V`, `Ctrl+v`                  |
| Command-line  | Modo de entrada de comandos, ativado com `:`                              |
| Select        | Texto escrito nesse modo substitui o texto antigo        |
| Ex            | Modo de linha de comando estendido, usado para comandos avançados         |

[Pesquisa](7_find.md)