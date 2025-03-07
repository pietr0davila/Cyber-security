# Linux
O *linux* é conhecido por ser um dos *SO* mais **rápidos e leves** possíveis, é **usado pelo TI** para *análise forense* e *hacking*. O linux pode ser complicado para uma pessoa que nunca usou aprender, mas depois você se acostuma

O linux é principalmente baseado em *linha de comando* e tem pouca GUI. No linux, você faz tarefas como **abrir ou baixar arquivos** diretamente pelo *Terminal* 

## Comandos de navegação
| Comando          | Descrição                                                      | Exemplo de Uso                        | Saída Exemplo                     |
| ---------------- | -------------------------------------------------------------- | ------------------------------------- | --------------------------------- |
| `echo`           | Exibe uma mensagem da sua escolha no terminal.                 | `root@linux1:~$ echo "Hello, world!"` | `Hello, world!`                   |
| `whoami`         | Bom pra quando você não sabe onde está logado                . | `root@linux1:~$ whoami`               | `root`                            |
| `ls`             | Revela todos os diretórios disponíveis no caminho.             | `root@linux1:~$ ls`                   | `a.txt text.txt documents folder` |
| `cd <diretório>` | Altera entre os diretórios.                          | `root@linux1:~$ cd documents`         | `root@linux1:~/documents $`       |
| `cat <arquivo>`  | Ler arquivos pequenos.                               | `root@linux1:~$ cat text.txt`         | `Conteúdo do arquivo text.txt`    |
| `pwd`            | Te mostra o caminho absoluto completo.                         | `root@linux1:~/documents $ pwd`       | `/home/ubuntu/Documents`          |

**Nota: arquivos ocultos (representados por . E.g: .ssh) podem ser incluidos no comando ls com o parâmetro -a (all)
## Comandos de pesquisa
| Comando | Descrição | Exemplo | Saída |
|---------|-----------|---------|-------|
| `find`  | O comando para procurar arquivos em qualquer lugar. | `find -name passwd.txt` | `./documents/.senhas.txt` |
| `grep`  | Vai procurar o texto que você pedir dentro de um arquivo. | `grep "senha" passwd.txt` | `senha 1 - - !4CFF0` |

## Operadores de terminal
| Operador | Descrição | Exemplo | 
|----------|-----------|---------|
| `&`      | Executa comandos em segundo plano. | `comando &` |
| `&&`     | Combina comandos, onde o segundo só roda se o primeiro der certo. | `comando1 && comando2`  |
| `>`      | Redireciona a saída pra um arquivo, substituindo o conteúdo se o arquivo já existir. | `echo "conteúdo" > arquivo.txt` |
| `>>`     | Adiciona a saída ao final de um arquivo sem apagar o que já estava lá. | `echo "mais conteúdo" >> arquivo.txt` | 

[próxima aula](fundamentospt2.md)