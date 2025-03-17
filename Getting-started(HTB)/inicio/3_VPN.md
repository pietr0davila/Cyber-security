# Aula 3

## Rede privada virtual (VPN)

Uma Virtual private network te conecta a redes internas com hosts e recursos que seriam inacessíveis publicamente

Geralmente é usado por empresas para que os funcionários acessem a rede interna da corporação do home office por exemplo

VPNs são usadas por que: 
1. serem seguras
2. permitirem a conexão de uma rede publica em uma rede privada
3. prevenirem a interceptação de dados (dados em trânsito e recebidos)

Tecnicamente uma VPN roteia a conexão internet pública do dispositivo atual diretamente do servidor privado ao invés do servidor do provedor. Ao se conectar a VPN seu IP é alterado

### SSL VPNs

usam o navegador como cliente VPN. A conexão é estabelecida entre o navegador e um (SSL VPN gateway)[https://www.twingate.com/blog/ssl-vpn]. São redes que permitem a conexão sem nenhuma instalação por parte do cliente

### Client-based VPNs

Require o uso de um software externo para estabelecer a conexão. Uma vez conectado você terá acesso a softwares, hosts, sub-redes e qualquer outro recurso dentro da rede da empresa

## Por que usar VPNs?

Podemos usar vpns no dia-a-dia para

1. Se conectar remotamente a servidores de outros países e acessar conteúdos indisponíveis no brasil
2. Alterar seu IP para mais privacidade

desvantagens incluem a possibilidade da vpn não armazenar os dados que deveriam ser armazenados e não seguir as melhores práticas de seguranças

Uma vpn pode ser muito importante para contornar firewalls e restrições de rede, principalmente no escopo da cibersegurança. Ou quando você se conectar a uma rede wi-fi pública

[Próxima aula](4_termos-comuns.md)
[hackthebox.com](../../README.md)