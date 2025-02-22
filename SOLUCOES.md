# Registro dos comandos usados para os desafios do ```Command Line Challenges```

## **Desafios e Soluções**

####    P1-B
utilizei o comando `tar`, ele é amplamente usado no linux para desempacotar e empacotar arquivos.

*Comando utilizado*
```bash
  tar -xvzf challenges.tar.gz
``` 
---

####    P2-B
utilizei o comando `cd <nome-do-diretorio>` porque já estava no mesmo diretório em que a pasta estava visível. Mas o comando dessa forma `cd <caminho/para/pasta>` também serve.

*Comando utilizado*
```bash
  cd challenges
``` 
---
####    P3-B
é só utilizar o comando `ls` depois de ter entrado no diretório _challenges_ no desafio anterior, ele irá listar todos arquivos e diretórios dentro do diretório atual.

*Comando utilizado*
```bash
  ls
```
---
####    P4-B
comando `mkdir <nome do diretorio>` para criar um diretório, acredito que assim como `ls` e o `cd` são comandos bem conhecidos também no windows.

*Comando utilizado*
```bash
  mkdir foo
``` 
---
####            P5-i:
O primeiro comando que me veio a cabeça foi `mkdir foo && cd foo mkdir bar && cd bar && mkdir 1 && cd 1 && mkdir 2 && cd 2 && mkdir 3` mas pela lógica, ele pareceu um pouco confuso apesar de funcional. Então, pesquisei e existe uma forma muito mais simples e ainda diminui as chances de erro. Além disso, aparentemente é necessário a flag `-p`.

*Comando utilizado*
```bash
  mkdir -p foo/bar/1/2/3    
```
---
####    P6-B
pensando no desafio anterior, tentei seguir a mesma lógica que usei e funcionou mas, é necessário ir do último diretório pro inicial -> `rmdir foo/bar/1/2/3 && rmdir foo/bar/1/2 && rmdir foo/bar/1 && rmdir foo/bar && rmdir foo` e foi funcional, mas aqui novamente a flag -p deixa o comando bem mais simples e enxuto.

*Comando utilizado*
```bash
  rmdir -p foo/bar/1/2/3
```
---
####            P7-B
o comando pra printar uma linha de texto é o `echo`.

*Comando utilizado*
```bash
  echo "Hello World"
```
---
####            P8-B
o mesmo comando que faz um print de uma string, também pode ser usado para inserir a string no arquivo caso não exista, se existir ele é sobrescrito `echo 'texto escolhido' > <nome-do-arquivo>.txt`.

*Comando utilizado*
```bash
  echo "Hello world" > hello.txt
```
---
####            P9-B
o comando pra realizar a tarefa é o `cat <nome do arquivo>.txt > <nome do arquivo>.txt`
ele criará um arquivo vazio com o nome escolhido.

*Comando utilizado*
```bash
  cat empty.txt > empty.txt
```
---
####            P10-B
aqui o comando pra realizar o desafio é o `rm <nome do arquivo>` ele removerá o arquivo que for passado pra ele e em caso de erro, ele avisa o que aconteceu.

*Comando utilizado*
```bash
  rm empty.txt
```
---
####            P11-I
aqui eu voltei na lógica do desafio que pediu pra criar um arquivo com texto, e testei pra ver se o echo também poderia ser usado para esse fim, e funcionou.

*Comando utilizado*
```bash
  echo "" > empty.txt
```
---
####            P12-I
nesse caso, por um erro acabei descobrindo que da pra criar arquivos usando apenas o comando 
`> <nome do arquivos>` (e aparentemente, há mais formas ainda de criar um arquivo).

*Comando utilizado*
```bash
  > empty.txt
```
---
####            P13-B
aqui o comando usado foi o `cp <nome do arquivo a ser copiado> <novo nome para o arquivo copiado>`. Ao utilizá-lo você informa o arquivo que quer copiar e qual será seu novo nome.

*Comando utilizado*
```bash
  cp hello.txt goodbye.txt
```
---
####            P14-B
aqui o comando usado foi o `mv <nome do arquivo> <novo nome do arquivo>`. Esse comando apenas altera o nome do arquivo, ele não copia. Ele também pode ser usado para mover um arquivo mas ai sua declaração será diferente.

*Comando utilizado*
```bash
  mv goodbye.txt hello_copy.txt
```
---
####            P15-I
o comando utilizado foi o `diff <nome de um arquivo a comparar> <nome do segundo arquivo>`. Ele compara o conteúdo dos dois arquivos e caso sejam iguais ele não mostra nada no terminal, caso sejam diferentes ele mostrará o conteúdo de ambos.

*Comando utilizado*
```bash
  diff hello.txt hello_copy.txt
```
---
####            P16-B
o comando utilizado foi o `cat <nome de um arquivo> <nome do segundo arquivo> > <nome do arquivo com o resultado da concatenação>`. como ele foi usado anteriormente, lembrei que ele servia para concatenar, tentei usar a lógica pra criar o arquivo dado os últimos exemplos e funcionou.

*Comando utilizado*
```bash
  cat hello.txt hello_copy.txt > 2_hellos.txt
```
---
####            P17-B
o comando usado aqui foi o `pwd` ele mostra o caminho completo para o diretório em você estiver atualmente.

*Comando utilizado*
```bash
  pwd
```
---
####            P18-B
o comando usado aqui foi o `ls` novamente. No entanto, dessa vez com a flag `-l` para que além de mostrar os arquivos no diretório, também mostre suas respectivas permissões.

*Comando utilizado*
```bash
  ls -l
```
---
####            P19-B
o comando usado aqui foi o `echo` novamente. No entanto, dessa vez da seguinte maneira `echo "<texto qualquer>" >> <nome do arquivo>`. o uso de `>>` faz com que em vez de sobrescrever o que está no arquivo, seja adicionado ao fim.

*Comando utilizado*
```bash
  echo "some text added." >> restricted.txt
```
---
####            P20-B
o comando usado aqui foi o `./<nome do arquivo a executar>`. ao executar esse comando no terminal, ele irá executar o arquivo com o nome especificado.

*Comando utilizado*
```bash
  ./hello_executable
```
---
####            P21-B
o comando usado aqui foram dois, primeiro o `chmod <permissão> <nome do arquivo>`. Porque o arquivo do desafio não possuia a permissão para poder executá-lo, foi necessário o uso do chmod para conceder essa permissão e em seguida utilizar o comando 
`./challenge_20`

*Comando utilizado*
```bash
  chmod +x challenge_20 && ./challenge_20
```
---
####            P22-B
aqui foi necessário `instalar o gcc` que é o compilador da linguagem C. E em seguida usar o `gcc` para fazer a versão compilada do arquivo `compile_me.c`.

**1° - instalar o gcc:**
```bash
  sudo apt install gcc
```
**2° - compilar o código com o gcc e executá-lo:**
```bash
    gcc compile_me.c -o compile_me && ./compile_me
```
---
####    P23-B
Geralmente a execução de um programa possui três saídas:

- Saída padrão (stdout): É a saída normal gerada pelo programa.

- Erro padrão (stderr): É onde os erros são enviados.

- padrão (stdin): É usada para enviar dados de entrada para o programa.

**E nesse desafio foi utilizado o comando `./<nome do programa> > <nome do arquivo> 2>&1`
o comando `2>&1` no final, avisa que o arquivo `output.txt` conterá tanto as mensagens de saída quanto as mensagens de erro.**

**Se não fosse usado o comando `2>&1`, dentro do output.txt haveria apenas o primeiro output e não tudo como pedia no desafio.**

*Comando utilizado*
```bash
    ./redirect > output.txt 2>&1
```
---
####    P24-B
para resolver esse desafio é só executar o comando `date`. Ele irá mostrar na tela a data e hora atual do sistema.

*Comando utilizado*
```bash
    date
```
---
####    P25-B
assim como no docker (pra quem conhece) no terminal do linux é possível usar o comando `ps` para conseguir verificar os processos que estão em execução. Pra ser mais exato `ps -e`. Mas existem mais flags que podem ser usadas nesse caso.

*Comando utilizado*
```bash
    ps -e
```
---
####    P26-B
o comando usado aqui foi o `nproc`. Ao executá-lo ele informará a quantidade de processadores do seu sistema

*Comando utilizado*
```bash
    nproc
```
---
####    P27-B
o comando usado aqui foi o `uname -a`. Ao executá-lo, irá informar detalhes completos do sistema como a versão do Linux, nome do computador, etc.

*Comando utilizado*
```bash
    uname -a
```
---
####    P28-B
o comando usado aqui foi o `grep -r "texto que você quer encontrar" <nome do diretorio>`. Com ele você escolhe o texto que está procurando e diz o diretório, ao executá-lo será possível identificar em qual arquivo está contido o texto inserido.

*Comando utilizado*
```bash
    grep -r "You found the needle in the haystack!" bunch_of_files/
```
---
####    P29-B
o comando usado aqui foi o `head`. Com ele você pode especificar em qual arquivo você quer consultar e quantas linhas da seguinte forma `head -n <numero de linhas> <nome-exemplo>.csv`

*Comando utilizado*
```bash
    head -n 25 people.csv
```
---
####    P30-B
o comando usado aqui foi o `tail`. Com ele você pode especificar em qual arquivo você quer consultar e quantas linhas da seguinte forma `tail -n <numero de linhas> <nome-exemplo>.csv`
**(segue o mesmo padrao do head)**

*Comando utilizado*
```bash
    tail -n 25 people.csv
```
---
####    P31-I
o comando usado aqui foi aquele mesmo `diff` usado no desafio 15. Porquê? Ele naturalmente em caso de diferenças entre o conteúdo dos arquivos escolhidos, apenas mostrará o que está diferente. Mas para uma melhor visualização podemos ainda usar o `| grep "[<>]"` ao fim do comando para que ele deixe a visualização mais limpa.

*Comando utilizado*
```bash
    diff greeting1.txt greeting2.txt | grep "[<>]"
```
---
####    P32-I
aqui utilizei uma combinação do `sleep` e o `echo`, o sleep para aguardar os 5 segundos do desafio e o echo para printar a string.

*Comando utilizado*
```bash
    echo "Hello" && sleep 5 && echo "world!"
```
---
####    P33-I
nesse desafio foi necessário utilizar o comando `dd` do seguinte modo:

*Comando utilizado*
```bash
    dd if=/dev/zero of=arquivo.txt bs=1M count=1
```

- **if=/dev/zero -** Especifica que o conteúdo do arquivo será preenchido com zeros.

- **of=arquivo.txt -** Define o nome do arquivo de saída (você pode escolher o nome que quiser).

- **bs=1M -** Define o tamanho do bloco como 1 MB.

- **count=1 -** Cria 1 bloco, ou seja, o arquivo terá 1 MB.

**obs: esse não é o único jeito de criar o arquivo desse desafio.**

---
####    P34-I
nesse desafio foi necessário reutilizar o comando `dd`, que usei no desafio anterior, do seguinte modo:

*Comando utilizado*
```bash
    dd if=/dev/urandom of=arquivo_aleatorio.txt bs=1M count=2
```
- **if=/dev/urandom -** Gera dados aleatórios.
- **of=arquivo_aleatorio.txt -** Define o nome do arquivo de saída.
- **bs=1M -** Define o tamanho do bloco como 1 MB.
- **count=2 -** Especifica que serão criados 2 blocos, ou seja, 2 MB.

---
####    P35-I
nesse desafio o comando utilizado foi o `wc` (word count), seguido da tag -l. Para usá-lo é necessário informar o nome do arquivo dessa forma: `wc -l <nome do arquivo>`, no entanto assim ele retornará a quantidade de linhas seguida do nome do Arquivo especificado.

**Caso queira que seja informado apenas o numero de linhas do arquivo, execute o comando da seguinte forma: `wc -l < <nome do arquivo>`**

*Comando utilizado*
```bash
    wc -l < README.txt
```
---
####    P36-B
para resolver esse desafio foi necessário apenas fazer uso do comando `tac`, ele exibe as linhas de um arquivo na ordem inversa, exatamente o que se pede no exercício.
`tac <nome do arquivo>`.

*Comando utilizado*
```bash
    tac README.txt
```
---
####    P37-I
nesse desafio foi necessário utilizar o comando `awk -F',' 'NR > 1 {print $2}' <nome do arquivo>`

**-F','**   Define a vírgula como delimitador.

**NR > 1**    Ignora a primeira linha (cabeçalho).

**$2**    Seleciona a segunda coluna.

*Comando utilizado*
```bash
    awk -F',' 'NR > 1 {print $2}' people.csv
```
---
####    P38-A
aqui novamente foi usado o comando `awk`. No entanto dessa vez com novas propriedades para ser possível identificar a quantidade de nomes únicos no arquivo do desafio.

**São elas:**
- **sort** Ordena os valores (necessário para usar uniq).

- **uniq** Remove duplicatas.

- **wc -l** Conta o número de linhas únicas.

*Comando utilizado*
```bash
    awk -F',' 'NR > 1 {print $2}' people.csv | sort | uniq | wc -l
```
---
####    P39-A
desde o primeiro exercício onde foi usado o comando `awk`, em seguida também foi usada a propriedade `NR > 1` ela automaticamente começa a contagem sem levar em conta o cabeçalho.

---
####    P40-A
nesse desafio uma outra forma que encontrei de contar os nomes únicos do arquivo sem contar com o cabeçalho/header foi substituindo o `NR > 1` pelo `grep`.

*Comando utilizado*
```bash
    grep -v "Last Name" people.csv | awk -F',' '{print $2}' | sort | uniq | wc -l
```

*Nesse caso, o `grep -v "Last Name"`, remove todas as linhas que contêm o texto "Last Name".*

---
####    P41-A
acrescentando o comando `time` ao início dos dois códigos realizados nos exercícios anteriores para encontrar os nomes únicos do arquivos `people.csv` foi possível notar que há um atraso maior na busca desses nomes quando é realizado o uso do comando `grep`. Acredito que isso se dá porque o comando grep é um comando extra na linha de comando quando combinado com o `awk`.**


- *Menos eficiente*
```bash
    time grep -v "Last Name" people.csv | awk -F',' '{print $2}' | sort | uniq | wc -l 
```
- *Mais eficiente (Comando utilizado)*
```bash
    time awk -F',' 'NR > 1 {print $2}' people.csv | sort | uniq | wc -l 
```
---
####    P42-A
O comando usado aqui foi novamente o `awk` mas com novas propriedades, para que seja possível identificar quantas pessoas possuem o primeiro nome "Josiah" no arquivo people.csv

*Comando utilizado*
```bash
    awk -F',' '$4 == "Josiah" {count++} END {print count}' people.csv
```
**Explicando as novas propriedades:**

- **$4 == "Josiah"** Verifica se o primeiro nome na coluna 4 (first name) é "Josiah".
- **count++** Conta quantas vezes o nome aparece.
- **END {print count}** Exibe o total de ocorrências após o processamento do arquivo.
---
####    P43-I
aqui, para contar o número de arquivos no diretório *challenges* foi necessário combinar novamente alguns comandos, como o `grep` e o `ls`.

*Comando utilizado*
```bash
    ls -l | grep -v '^d' | wc -l
```
- **ls -l** - lista todos os arquivos no diretório
- **grep -v '^d'** - Filtra a saída para excluir linhas que começam com "d" (indicando que é um diretório).
- **wc -l** - Conta o número de linhas da saída filtrada, nesse caso, o número de arquivos.

**OBS:** Nesse caso, não foi especificado para o `ls` o diretório *porque o comando foi executado dentro do diretório challenges*, mas poderia ser feito da seguinte forma:
`ls -l <caminho para o diretório ou nome do diretório disponível> | grep -v '^d' | wc -l`
---
####    P44-I
Nesse desafio, novamente foi utilizado uma combinação do comando `ls`e `grep` mas com assinaturas diferentes das usadas anteriormente.

*Comando utilizado*
```bash
    ls -l | grep '^d' | wc -l
```
*é possível notar que aqui há a ausência da flag -v no comando `grep` que foi usada anteriormente para filtrar.*

---
####    P45-I
aqui foi utilizado uma nova combinação de comandos. Resolvi combinar o comando `cd` com os comandos utilizados nos últimos exercícios para resolver esse. Entrei no diretório *challenges* e em seguida no subdiretório *bunch_of_files*, listei os arquivos, filtrei e em seguida passei os arquivos filtrados para o comando `rm` para que cada um dos arquivos do desafio fosse excluído.

*Comando utilizado*
```bash
    cd challenges/bunch_of_files && ls | grep 'deleteme' | xargs rm
```
- **grep 'deleteme'** - Filtra os arquivos que contêm "deleteme" no nome.

- **xargs rm** - Passa os arquivos encontrados para o comando `rm` para que ele possa excluir cada um.

*OBS: não era necessário utilizar o `cd` aqui. Daria pra passar o diretório pelo próprio `ls` como foi exemplificado anteriormente. Foi só uma escolha pessoal pra fazer diferente.*

---
####    P46-I
nesse desafio foi necessário fazer uso de um novo comando, o `sed`. Dessa forma: `sed -i 's/texto_antigo/texto_novo/' <nome do arquivo.txt>`

na declaração do comando você diz o texto que você quer substituir e qual o novo texto que deverá ficar no lugar do antigo. Em seguida, deve informar em qual arquivo você quer que a alteração ocorra.

*Comando utilizado*
```bash
    sed -i 's/You found the needle in the haystack!/he needle has been removed./' file719.rand
```

- a flag `-i` Modifica o arquivo diretamente (faz a substituição no próprio arquivo, sem criar uma cópia).

*E claro, aqui foi necessário buscar o nome do arquivo que continha a mensagem do desafio. Nesse sentido, reutilizei o mesmo código do desafio 28 para identificar o nome do arquivo desejado.*

---
####    P47-A
aqui foi fácil, com base no desafio anterior foi preciso apenas reutilizar o comando do desafio para a finalidade do desafio atual. Porém, houve a necessidade de acrescentar duas mudanças.

*Comando utilizado*
```bash
    sed 's/,/|/g' people.csv > people_pipe.csv
```
- *aqui foi necessário acrescentar dentro de `'s/,/|/g'` o `g` que não estava presente anteriormente. Caso o comando seja executado sem ele, a mudança não será implementada em todas as `,` (vírgulas) do arquivo. A mudança ocorreria apenas na primeira linha.*
- *para salvar em um novo arquivo foi usado `> people_pipe.csv`, dessa forma as mudanças estão presentes apenas no novo arquivo.*
---
####    P48-A
nesse desafio foi necessário utilizar novos comandos para finalizá-lo. o comando utilizado foi o `find`.

*Comando utilizado*
```bash
    find -type f -exec cmp --silent file001.rand {} \; -print
```
- **find </caminho/do/diretorio>** - Procura por arquivos no diretório. *no caso se você já estiver com o diretório aberto e quiser apenas buscar dentro dele, pode chamar o `find`sem passar o caminho para um diretório que ele fará a busca no diretório atual.*
- **-type f** - Filtra para procurar apenas arquivos (e não diretórios).
- **cmp --silent file001.rand {}** - Compara o arquivo file001.rand com cada arquivo encontrado. O parâmetro --silent faz com que cmp não produza saída, apenas retorne o status de comparação.
- **print** - Exibe o caminho dos arquivos que são idênticos ao arquivo original.
---
####    P49-A
aqui para não perder os outros arquivos dos desafios já realizados, realizei os dois exercícios do desafio do seguinte modo:

- criei um diretório com o nome `desafio-49`, criei o arquivo `supercalifragilisticexpialidocious.txt` e o enviei para o diretório criado.
```bash
    mkdir desafio-49 | > supercalifragilisticexpialidocious.txt | mv supercalifragilisticexpialidocious.txt desafio-49
```
- para completar o desafio com um comando que não exceda os 5 caracteres usei o `rm` mesmo.
```bash
    rm ./*
```
---
####    P50-A
nesse desafio existem várias maneiras de conseguir finalizá-lo. No entanto, tentar manter um número menor de caracteres como foi a pergunta desse desafio, é mais difícil.

*Caso seu bash tenha suporte para expansão de chaves*

*Comando utilizado*
```bash
    touch {a..c}-{1..3}.txt
```

_A expansão de chave (ou brace expansion) é um recurso do shell (como o Bash) que permite gerar automaticamente listas de strings com base em um padrão definido entre chaves {}. Ela é usada para criar combinações de valores sem precisar escrever cada um manualmente, economizando tempo e escrita_

*Exemplo de expansão de chaves*
```bash
    echo {a,b,c}-{1..3}
```
_output:_

    a-1 a-2 a-3 b-1 b-2 b-3 c-1 c-2 c-3
---
