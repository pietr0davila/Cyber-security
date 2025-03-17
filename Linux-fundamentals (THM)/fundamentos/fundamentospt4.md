# Gerenciamento de pacotes

Algumas ferramentas podem ser baixadas muito mais rapidamente usando o *apt*. Quando um dev publica um software. ele pode enviar ele para o repositório apt. se ele for aprovado o comando `apt install [software]` pode baixar esse software

O apt faz parte do **Advanced package tools**, caso queira adicionar um repositório ao apt pode usar o comando `add-apt-repository` ou fazer isso manualmente

# Logs

Logs são arquivos que documentam tudo o que acontece no servidor

## Exemplos

### Servidor apache
access.log: registra solicitações, em outras palavras guarda os ips de todos que entraram no site. Path: `/var/log/apache2/access.log`
error.log: Onde o servidor documenta erros. Path: `/var/log/apache2/error.log`

### Fail2Ban

fail2ban: site de prevenção de brute force. Path: `/var/log/apache2/fail2ban.log`

## UFW (Uncomplicated firewall)

ufw: registra atividades do firewall. Path: `/var/log/ufw.log`

## Logs São importantesw para
- Monitorar a saúde e integridade do sistema
- Identificar erros e falhas de software ou kernel
- Realizar auditorias e salvar históricos de atividade

## Logs comuns

### Error.log
Quando você tem um erro, pode procurar aqui 

### Access
salva todas as requisições http. guarda ip, data e hora e o recurso solicitado pelo cliente

## Logs do sistema

O sistema tem logs importantissímos

/var/log/sys.log: log onde o sistema armazena toda a atividade
/var/log/auth.log: Registra tentativas de autenticação, tanto bem tanto mal sucedidas
