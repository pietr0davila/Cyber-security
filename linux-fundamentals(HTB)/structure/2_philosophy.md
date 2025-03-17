# Aula 2

O centro da filosofia do linux é Simplicidade, modularidade e abertura. Defende a criação de scripts pequenos para realizar tarefas de forma eficiente. Esses arquivos podem se juntar com outros para realizar tarefas complexas. O linux tem 5 principios:

# Principios

| Princípio             | Descrição                                                      |
|-----------------------|----------------------------------------------------------------|
| Tudo é um arquivo | Arquivos de configuração são armazenados quase sempre em texto |
| Programas pequenos de propósito único | As ferramentas são criadas individualmente mas podem ser usadas em conjunto |
| Juntar programas pequenos para propósitos complexos | Podemos juntar comandos pequenos e executar tarefas complexas, mesmo que os arquivos individuais sejam leves |
| Evitar interface gráfica | O linux foi desenvolvido pra ser usado com o shell, o que da ao usuário controle total sobre o sistema, além de um sistema mais barato e leve |
| Arquivos de configuração em texto plano | Um exemplo é o /etc/passwd. que tem tds os usuários registrados |

# Componentes
| Componente | Descrição                                                                        |
| ---------- | ---------------------------------------------------------------------------------|
| *Bootloader* | **Guia a inicialização** do sistema. ParrotOS usa o GRUB BootLoader            |
| *OS Kernel*  | **Componente principal do sistema**, gerencia os recursos no nível de hardware |
| *Daemons*    | Arquivos de segundo plano executados depois do login para verificar o funcionamento de funções principais   |
| *OS Shell*   | A linha de comando é a **interface entre OS e usuário**. Um exemplo é o bash   |
| *Servidor gráfico* | Fornece um **subsistema gráfico** que permite a execução de *GUI¹* no Linux |
| *Gerenciador de janela* | Conhecido como GUI, permitem o **uso do sistema fora do terminal**  |
| *Utilidades* | Ou aplicações, são **programas com tarefas especificas** para o usuário ou para o sistema em si |

¹: GUI: Graphic user interface, ou GUI são interfaces menos técnicas e mais intuitivas do que o terminal

# Arquitetura do Linux
| camada | Descrição                                                                      |
| ----------- | ------------------------------------------------------------------------- |
| *Hardware*  | Periféricos como RAM, CPU e outros **objetos fisícos do sistema**         |
| *Kernel*    | Núcleo do sistema, a função principal é **virtualizar e controlar o hardware**. Divide recursos entre processos e impede conflitos entre eles                                                   |
| *Shell*     | Ou CLI, é onde o usuário pode **executar comandos do kernel** diretamente |
| *Utilidade do sistema* | **Torna as funcionalidades do sistema disponiveis** para o usuário |

# Hierarquia de arquivos do sistema

| caminho   | Descrição                                                                                        |
| --------- | ------------------------------------------------------------------------------------------------ |
|  **/**    | É o diretório de nível mais alto, deve ser carregado antes de todo o resto e é essencial para iniciar o sistema, todos os diretórios são subdiretórios desse, é chamado de diretório root                              |
| **/bin**  | Contém comandos binários essenciais                                                              |
| **/boot** | Bootloader estático, inicializador do kernel e arquivos necessários para inicializar o linux     | 
| **/dev**  | Arquivos do dispositivo para facilitar o acesso ao hardware associado ao sistema                 |
| **/etc**  | Arquivos de configuração do sistema. Arquivos de configuração externo também podem ser instalados aqui |
| **/home** | Cada usuário tem um subdiretório aqui                                                            |
| **/lib**  | Bibliotecas essenciais para a inicialização do sistema                                           |
| **/media**| Dispositivos removiveis externos, como drives USB são montados aqui                              |
| **/mnt**  | Ponto temporário de montagem de arquivos do sistema                                              |
| **/opt**  | Arquivos opcionais como ferramentas costumam ser armazenados aqui                                |
| **/root** | Diretório Home mas para o super usuário (root)                                                   |
| **/sbin** | Contém binários executáveis para administração do sistema                                        |
| **/tmp**  | Contém dados temporários armazenados pelo sistema ou aplicativos, costumam ser apagados no boot  |
| **/usr**  | user system resources, tem tudo que o usuário pode usar (Como executáveis e bibliotecas)         | 
| **/var**  | Contém dados variáveis (Como logs, crontabs e outros)                                            |
![Hierarquia](/content/hierarquia-de-arquivos.png)

[font](https://academy.hackthebox.com/module/18/section/94)
[Aula 3](../distros/3_linux-distros.md)