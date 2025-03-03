Na área de segurança, organização é essencial. é importante ter uma documentação clara e concisa desde o começo. Isso te deixa a frente de muitos canditados e ainda garante que você consiga voltar atrás se necessário

## Estrutura de pastas

Ao atacar um alvo isolado ou controlado, precisamos de uma estrutura de pastas clara para armazenar escopo, enumeração, evidências e tentativas de exploit, dados como credenciais ou outro dados obtidos durante a exploração:

```
Projects/

└── Acme Company

├── EPT

│ ├── evidence

│ │ ├── credentials

│ │ ├── data

│ │ └── screenshots

│ ├── logs

│ ├── scans

│ ├── scope

│ └── tools

└── IPT

├── evidence

│ ├── credentials

│ ├── data

│ └── screenshots

├── logs

├── scans

├── scope

└── tools
```


Temos uma pasta para cada cliente (ACME company) com 2 subpastas Internal penetration testing e external penetration testing. Em cada subpasta dentro dessa temos dados, credenciais e capturas de telas úteis

Produtividade e organização são importantes, um relatório detalhado e desorganizado tem a mesma utilidade de um relatório raso bem-organizado (nenhuma)

Manter listas de verificação, modelos de relatório para avaliações diferentes e um banco de dados descobertas/vulnerabilidades, o banco de dados pode ser uma planilha ou algo complexo com título, descrição impacto, remediação e referência. Ter isso escrito facilita na hora de montar um relatório final

[Próxima aula](3_VPN.md)
[hackthebox.com](https://academy.hackthebox.com/module/77/section/766)

