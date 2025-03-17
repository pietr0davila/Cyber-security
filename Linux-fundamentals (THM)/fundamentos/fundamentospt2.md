# Fundamentos linux pt2

## Comandos de manipulação de arquivo

| Comando | Nome Completo     | Função                         |
|---------|-------------------|--------------------------------|
| touch   | touch             | Criar um arquivo               |
| mkdir   | make directory    | Criar um diretório             |
| rmdir   | remove directory  | Remover um diretório           |
| rm      | remove            | Remover um arquivo             |
| mv      | move              | Mover um arquivo ou diretório  |
| cp      | copy              | Copiar um arquivo ou diretório |
| file    | file              | Determinar o tipo de arquivo   |

**Obs: mv pode renomear um arquivo. E.g: mv arquivo.txt arquivo.md**

`touch arquivo.txt`

Cria um arquivo vazio (de texto nesse caso)

`mkdir projetos`

Cria um diretório no caminho atual

`rm arquivo.txt`

Apaga o arquivo *arquivo.txt*

`rmdir projetos`

Apaga o diretório

Bônus:
`rmdir -R documents`
Apaga o diretório e tudo que tiver dentro dele

`cp arquivo.txt /home/ubuntu`

Copia um arquivo para outro diretório
1° parâmetro: arquivo
2° parâmetro: caminho da cópia

mv para mover
`mv arquivo.txt /root`
mv para renomear
`mv arquivo.txt archive.text`

`file arquivo.txt`

Verifica o tipo do arquivo, nesse caso txt. Útil quando precisamos saber o conteúdo de um arquivo sem extensão

## Permissões

ls -lh mostra o que cada usuário pode fazer com arquivos

### SSH

Temos uma aula sobre ssh em [SSH](/Getting-started(HTB)/pentesting-basico/protocolos/prot4_ssh.md)

Temos uma aula do comando padrão de SSH, mas para recaptular
`ssh root@10.10.10.15`

Onde root representa o usuário que você vai conectar e 10.10.10.15 representa o ip do servidor.

**Nota: SSH não tem feedback visual, e o linux no geral, então quando você escrever uma senha, não estranhe se não ver ela**

## Troca rápida de usuário
O comando su troca o usuário atual para o superusuário/root, claro, só no terminal

`su`

# Diretório padrão

/etc: Arquivos de configuração do linux
/var: todos os dados variáveis incluindo mas não tse limitando a logse backups
/root: é o diretório home do superusuário
/tmp: arquivos armazenados na memória RAM (que vão ser apagados no reinicio do sistema) ficam aí

# Parâmetros
Parâmetros são maneiras de adicionar dados ou pedir uma saída personalizada ao comando, cada ferramenta tem seus parâmetros. E.g:

`nmap 10.10.10.15`

onde nmap é a execução do nmap e 10.10.10.15 é um parâmetro com o ip

[Próxima aula](fundamentospt3.md)