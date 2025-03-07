# Editores de texto

## Nano

Para abrir um arquivo com nano:
`nano arquivo.txt`

Para navegar entre as linhas você usa as setas do teclado
Salvar, ctrl + O
Sair, ctrl + X

## Vim

Temos uma aula sobre vim em [vim](/Getting-started(HTB)/pentesting-basico/5_ferramentas.md#vim)

# Baixar arquivos com wget
Sabe quando você vai instalar um software apertando aquele botão vermelho gigante no navegador? é exatamente isso, só que pelo terminal
`wget https://XXXXX.XXXXXX/XXXXX.XXXXXX/XXXXXXXXXXX-XXXXXX/XXXX/XXX/arquivo.txt`
Ele é útil para interfaces sem GUI como servidores por exemplo e pode ajudar a automatizar um software, por exemplo re-instalar em um certo periodo de tempo pra atualizar

# Transferência de arquivos com scp
scp é secure copy, ele permite que você disponibilize arquivos da sua máquina para uma externa ou vice-versa. ele é criptografado

transferência da máquina local > remota

`scp arquivo.txt ubuntu@205.102.220.55:/home/ubuntu/transfer.txt`
onde arquivo.txt é o arquivo que você vai transferir.
ubuntu@... é quem vai receber o arquivo
:/home/... é o diretório pra onde vai ser transferido

Ao contrário
`scp ubuntu@10.10.10.15:/home/ubuntu/documents.txt arquivo.txt`

você deve ter percebido que só a ordem mudou, no primeiro comando especificamos o arquivo o e depois o alvo e no segundo o alvo e o caminho do arquivo

Scp só funciona com credenciais ssh

## Base64

Você pode criptografar o arquivo em base 64, enviar para o alvo e descriptografar. Isso é usado para burlar firewalls

No host local:
`base64 shell -w 0`

No host remoto:
`echo "...." | base64 -d > shell`

# SErvidor local

A maneira mais comum de servir arquivos em uma rede externa é baixando os dados do seu sistema no sistema comprometido. Para servir esses arquivos do seu computador você pode usar o python
`python3 -m http.server` 

Esse servidor funciona na porta 8000 e só funciona enquanto essa janela estiver aberta

# Processos 
O comando ps aux te mostra tudo acontecendo no pc, como ram gasta e processos

O comando `kill` pode encerrar qualquer processo. Existem 3 tipos de encerramento

SIGTERM: Permite que o processo termine de executar a tarefa atual antes de desativar, pode ser ignorado dependendo da forma como foi desenvolvido
SIGKILL: Desativa o processo de uma vez. Não permite que o processo manipule ou ignore o comando e vai parar de ser executado independente do que estiver fazendo
SIGSTOP: Desativa o processo mas não apaga da memória, pode ser continuado usando SIGCONT

O comando systemctl pode fazer um script ou programa ser iniciado ao ligar o pc.

`systemctl start apache2`
Inicia o apache sempre que a máquina ligar
`systemctl stop apache2`
Você pode parar o processo

# Primeiro e segundo plano

o operador & permite que um comando rode em segundo plano enquanto você faz outra coisa

`wget https://google.com/button.exe &`

Baixa o arquivo em segundo plano

# crontabs

Podem ser usadas para executar tarefas periódicas, como back-ups. Cada crontab tem 6 parâmetros

MIN - minute
HOUR - hour
DOM - day of month
MON - month
DOW - Day of week
CMD - Command

`0 */12 * * * cp -R /home/usuario/documentos/ /var/backups`

\* (wild cards): indicam que vai ser executado a todo momento do parâmetro

[crontab generator](https://crontab-generator.org/) pode gerar crontabs automaticamente


[próxima aula](fundamentospt4.md)