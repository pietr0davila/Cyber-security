# Public & Private keys
O SSH funciona assim, temos 2 chaves geradas pelo cliente, uma pública (enviada ao servidor e armazenada em um diretório como ~/.ssh/authorized_keys). Quando o usuário tenta se conectar ao sistema SSH, o servidor envia um tipo de "desafio criptografado" com a chave pública do usuário. O usuário descriptografa o desafio com a sua chave privada e envia de volta ao servidor. se o cliente retornar o desafio corretamente, o servidor valida o acesso

A criptografia de chaves públicas e privadas é muito usada em sistemas cruciais para o funcionamento da internet, por exemplo o protocolo TLS/SLL que possibilita o acesso seguro a sites usando HTTPS. Esse tipo de criptografia é chamado de criptografia assimétrica, pois as chaves são diferentes e uma não pode ser usada para descriptografar a outra.

[fonte](https://www.cloudflare.com/pt-br/learning/ssl/how-does-public-key-encryption-work/)