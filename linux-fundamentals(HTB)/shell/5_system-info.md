# Aula 5
No linux, é importante entender a estruturam incluindo detalhes do sistema, processos, configuração de rede, configuração de usuário(s) e diretórios. Os comandos abaixos são úteis para usar o linux no cotidiano e para acessar, configurações mal definidas, dados vazados, credenciais, identificar vulnerabilidades

| Comando   | Descrição                                                                       |
|-----------|---------------------------------------------------------------------------------|
| whoami    | Exibe o nome do usuário atual.                                                 |
| id        | Retorna a identidade do usuário.                                               |
| hostname  | Define ou imprime o nome do host atual.                                        |
| uname     | Exibe informações básicas sobre o nome do sistema operacional e o hardware.   |
| pwd       | Retorna o nome do diretório de trabalho atual.                                 |
| ifconfig  | Utilitário usado para atribuir ou visualizar um endereço a uma interface de rede e/ou configurar parâmetros da interface de rede. |
| ip        | Utilitário para exibir ou manipular roteamento, dispositivos de rede, interfaces e túneis. |
| netstat   | Exibe o status da rede.                                                       |
| ss        | Outro utilitário para investigar sockets.                                      |
| ps        | Exibe o status dos processos.                                                 |
| who       | Mostra quem está conectado.                                                   |
| env       | Imprime as variáveis de ambiente ou define e executa comandos.                |
| lsblk     | Lista dispositivos de bloco.                                                  |
| lsusb     | Lista dispositivos USB.                                                       |
| lsof      | Lista arquivos abertos.                                                       |
| lspci     | Lista dispositivos PCI.                                                       |

Importância do id:
`uid=1000(cry0l1t3) gid=1000(cry0l1t3) groups=1000(cry0l1t3),1337(hackthebox),4(adm),24(cdrom),27(sudo),30(dip),46(plugdev),116(lpadmin),126(sambashare)`

Usado por pentesters para descobrir qual acesso um usuario pode ter
Administradores também podem usar para auditar associações e pemissões.
O grupo adm indica que o usuário tem acesso aso arquivos 
O grupo sudo indica que o usuário pode executar um ou todos os comandos como root


# Aula 5 pt2

## Secure Shell SSH

Protocolo que permite execução de código remoto. Em dispositivos e servidores linux-based (e alguns Unix-like) é uma ferramenta instalada por padrão permanentemente. O comando para se conectar remotamente a outro dispositivo usando o SSH é:

`[!bash!] ssh <user>@<ip>`

