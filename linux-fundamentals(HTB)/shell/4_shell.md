# Aula 4

Um terminal linux é uma linha de comando baseada em entrada e saída (I/O) entre usuário e kernel. o shell é uma graphic User Interface (GUI) onde enviamos comandos para navegar, usar arquivos e obter dados do sistema sem limitações

Um emulador de terminal é um software que emula a função do terminal, ele é a janela que você usa ao acessar o terminal. CLI (Command-Line interface) é o conjunto de comandos (bash) executados para se comunicar com o kernel

## Shell

o usado no linux na maioria das vezes é o Bourne-Again Shell (BASH). No linux, tudo que você pode acessar com a GUI você pode acessar com o shell. O shell permite interagir com programas e procesos pra conseguir informações mais rápido

[font](https://academy.hackthebox.com/module/18/section/65)

# aula 4 - pt2 
## Descrição do prompt

O bash é ismples de entender. as informações que ele fornece são respectivamente:
- seu usuário
- o nome do seu computador (hostname)
- diretório atual
`<N1bble>@<anthem>[~]$`

O diretório home do seu usuário sempre é representado com '~' e é a pasta padrão quando você abre o emulador. O sinal de dólar representa o shell do usuário. O shell do root é representado por '#'

`root@anthem[/htb]#`

Quando um reverse-shell de qualquer tipo é upado, vemos o shell com quase nenhuma informação, só o '$' ou '#'. Isso acontece pq a variável PS1 não foi configurada. Essa variável é tipo um template de como o terminal vai aparecer
Lista de opções personalizáveis

| Código       | Descrição                                       |
|--------------|------------------------------------------------ |
| \d           | Data (Seg 6 Fev)                                |
| \D{%Y-%m-%d} | Data (AAAA-MM-DD)                               |
| \H           | Nome completo do host                           |
| \j           | Número de trabalhos gerenciados pelo shell      |
| \n           | Nova linha                                      |
| \r           | Retorno de carro                                |
| \s           | Nome do shell                                   |
| \t           | Hora atual em formato 24h (HH:MM:SS)            |
| \T           | Hora atual em formato 12h (HH:MM:SS)            |
| \@           | Hora atual                                      |
| \u           | Nome de usuário atual                           |
| \w           | Caminho completo do diretório de trabalho atual |

Além das fontes, cores e outros dados configuráveis. O [bash prompt generator](https://bash-prompt-generator.org/) tem prompts diferentes e úteis

[font](https://academy.hackthebox.com/module/18/section/66)
# Aula 4 - pt3

## MAn
o comando man é usado para exibir páginas de manual de comandos (não todos). exemplo:
```bash
[!bash!]$ man ls
LS(1)                            User Commands                           LS(1)

NAME
       ls - list directory contents

SYNOPSIS
       ls [OPTION]... [FILE]...

DESCRIPTION
       List  information  about  the FILEs (the current directory by default).
       Sort entries alphabetically if none of -cftuvSUX nor --sort  is  speci‐
       fied.

       Mandatory  arguments  to  long  options are mandatory for short options
       too.

       -a, --all
              do not ignore entries starting with .

       -A, --almost-all
              do not list implied . and ..

       --author
 Manual page ls(1) line 1 (press h for help or q to quit)
```
A maioria dos comandos tem um argumento de ajuda, normalmente --help ou -h, esse comando indica quais são os parâmetros e a sintaxe do comando
```bash
ls --help

Usage: ls [OPTION]... [FILE]...
List information about the FILEs (the current directory by default).
Sort entries alphabetically if none of -cftuvSUX nor --sort is specified.

Mandatory arguments to long options are mandatory for short options too.
  -a, --all                  do not ignore entries starting with .
  -A, --almost-all           do not list implied . and ..
      --author               with -l, print the author of each file
  -b, --escape               print C-style escapes for nongraphic characters
      --block-size=SIZE      with -l, scale sizes by SIZE when printing them;
                             e.g., '--block-size=M'; see SIZE format below

  -B, --ignore-backups       do not list implied entries ending with ~
  -c                         with -lt: sort by, and show, ctime (time of last
                             modification of file status information);
                             with -l: show ctime and sort by name;
                             otherwise: sort by ctime, newest first

  -C                         list entries by columns
<...>
```

```bash
[!bash!]$ curl -h

Usage: curl [options...] <url>
     --abstract-unix-socket <path> Connect via abstract Unix domain socket
     --anyauth       Pick any authentication method
 -a, --append        Append to target file when uploading
     --basic         Use HTTP Basic Authentication
     --cacert <file> CA certificate to verify peer against
     --capath <dir>  CA directory to verify peer against
 -E, --cert <certificate[:password]> Client certificate file and password
<...>
```
[font](https://academy.hackthebox.com/module/18/section/67)
[aula 5](5_system-info.md)