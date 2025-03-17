Procurar arquivos de configuraçoes, arquivoes criados e etc é essencial

Which permite que você procure um software no path do sistema
```
which python
/usr/bin/python
```

find é usado para usar arquivos e diretórios, é possível filtrar resultados com tamanho do arquivo ou data

```anotherMan@htb[/htb]$ find / -type f -name *.conf -user root -size +20k -newermt 2020-03-03 -exec ls -al {} \; 2>/dev/null
-rw-r--r-- 1 root root 136392 Apr 25 20:29 /usr/src/linux-headers-5.5.0-1parrot1-amd64/include/config/auto.conf
<...>
-rw-r--r-- 1 root root 55285 May  7 14:33 /usr/share/metasploit-framework/data/jtr/dumb16.conf
-rw-r--r-- 1 root root 21254 May  2 11:59 /usr/share/doc/sqlmap/examples/sqlmap.conf
-rw-r--r-- 1 root root 25086 Mar  4 22:04 /etc/dnsmasq.conf
-rw-r--r-- 1 root root 21254 May  2 11:59 /etc/sqlmap/sqlmap.conf
```

| Opção | Descrição |
|-------|-----------|
| -type f | Define o tipo do objeto procurado. Neste caso, 'f' significa 'file'. |
| -name *.conf | Indica o nome do arquivo que estamos procurando. O asterisco (*) representa 'todos' os arquivos com a extensão '.conf'. |
| -user root | Filtra todos os arquivos cujo proprietário é o usuário root. |
| -size +20k | Filtra todos os arquivos localizados e especifica que queremos ver apenas os arquivos maiores que 20 KiB. |
| -newermt 2020-03-03 | Define a data. Apenas arquivos mais novos que a data especificada serão apresentados. |
| -exec ls -al {} \; | Executa o comando especificado, usando as chaves como placeholders para cada resultado. A barra invertida escapa o próximo caractere para não ser interpretado pelo shell, pois caso contrário, o ponto e vírgula terminaria o comando e não alcançaria o redirecionamento. |
| 2>/dev/null | Redirecionamento de STDERR para o 'dispositivo nulo', garantindo que nenhum erro seja exibido no terminal. Este redirecionamento não deve ser uma opção do comando 'find'. |

Isso demora muito para procurar o solicitado em cada pasta e subpasta, o ocmando locate é um banco de dados local e pode fazer isso
Atualiza o db
`sudo updatedb`

`locate *.conf`
    