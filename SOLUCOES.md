#   Registro dos comandos usados para os desafios do ```Command Line Challenges```

**p1-b: utilizei o comando `tar`, ele é amplamente usado no linux para desempacotar e empacotar arquivos.** 
```bash
  tar -xvzf challenges.tar.gz
``` 
---
**p2-b: utilizei o comando `cd <nome-do-diretorio>` porque já estava no mesmo diretório em que a pasta estava visível. Mas o comando dessa forma `cd <caminho/para/pasta>` também serve.**
```bash
  cd challenges
``` 
---
**p3-b: é só utilizar o comando `ls` depois de ter entrado no diretório _challenges_ no desafio anterior, ele irá listar todos arquivos e diretórios dentro do diretório atual.**
```bash
  ls
``` 
---
**p4-b: comando `mkdir <nome do diretorio>` para criar um diretório, acredito que assim como `ls` e o `cd` são comandos bem conhecidos também no windows.**
```bash
  mkdir foo
``` 
---
**p5-i: O primeiro comando que me veio a cabeça foi `mkdir foo && cd foo mkdir bar && cd bar && mkdir 1 && cd 1 && mkdir 2 && cd 2 && mkdir 3` mas pela lógica, ele pareceu um pouco confuso apesar de funcional. Então, pesquisei e existe uma forma muito mais simples e ainda diminui as chances de erro. Além disso, aparentemente é necessário a flag `-p`.**
```bash
  mkdir -p foo/bar/1/2/3    
```
---
**p6-b: pensando no desafio anterior, tentei seguir a mesma lógica que usei e funcionou mas, é necessário ir do último diretório pro inicial -> `rmdir foo/bar/1/2/3 && rmdir foo/bar/1/2 && rmdir foo/bar/1 && rmdir foo/bar && rmdir foo` e foi funcional, mas aqui novamente a flag -p deixa o comando bem mais simples e enxuto.**
```bash
  rmdir -p foo/bar/1/2/3
```
---
**p7-b: o comando pra printar uma linha de texto é o `echo`.**
```bash
  echo "Hello World"
```
---
**p8-b: o mesmo comando que faz um print de uma string, também pode ser usado para inserir a string no arquivo caso não exista, se existir ele é sobrescrito `echo 'texto escolhido' > <nome-do-arquivo>.txt`.**
```bash
  echo "Hello world" > hello.txt
```
---
**p9-b: o comando pra realizar a tarefa é o `cat <nome do arquivo>.txt > <nome do arquivo>.txt`
ele criará um arquivo vazio com o nome escolhido.**
```bash
  cat empty.txt > empty.txt
```
---
**p10-b: aqui o comando pra realizar o desafio é o `rm <nome do arquivo>` ele removerá o arquivo que for passado pra ele e em caso de erro, ele avisa o que aconteceu.**
```bash
  rm empty.txt
```
---
**p11-i: aqui eu voltei na lógica do desafio que pediu pra criar um arquivo com texto, e testei pra ver se o echo também poderia ser usado para esse fim, e funcionou.
O comando usado foi o `echo "" > empty.txt`**
```bash
  echo "" > empty.txt
```
---
**p12-i: nesse caso, por um erro acabei descobrindo que da pra criar arquivos usando apenas o comando 
`> <nome do arquivos>` (e aparentemente, há mais formas ainda de criar um arquivo).**
```bash
  > empty.txt
```
---
**p13-b: aqui o comando usado foi o `cp <nome do arquivo a ser copiado> <novo nome para o arquivo copiado>`. Ao utilizá-lo você informa o arquivo que quer copiar e qual será seu novo nome.**
```bash
  cp hello.txt goodbye.txt
```
---
**p14-b: aqui o comando usado foi o `mv <nome do arquivo> <novo nome do arquivo>`. Esse comando apenas altera o nome do arquivo, ele não copia. Ele também pode ser usado para mover um arquivo mas ai sua declaração será diferente.**
```bash
  mv goodbye.txt hello_copy.txt
```
---
**p15-i: o comando utilizado foi o `diff <nome de um arquivo a comparar> <nome do segundo arquivo>`. Ele compara o conteúdo dos dois arquivos e caso sejam iguais ele não mostra nada no terminal, caso sejam diferentes ele mostrará o conteúdo de ambos.**
```bash
  diff hello.txt hello_copy.txt
```
---
**p16-b: o comando utilizado foi o `cat <nome de um arquivo> <nome do segundo arquivo> > <nome do arquivo com o resultado da concatenação>`. como ele foi usado anteriormente, lembrei que ele servia para concatenar, tentei usar a lógica pra criar o arquivo dado os últimos exemplos e funcionou.**
```bash
  cat hello.txt hello_copy.txt > 2_hellos.txt
```
---
**p17-b: o comando usado aqui foi o `pwd` ele mostra o caminho completo para o diretório em você estiver atualmente.**
```bash
  pwd
```
---
**p18-b: o comando usado aqui foi o `ls` novamente. No entanto, dessa vez com a flag `-l` para que além de mostrar os arquivos no diretório, também mostre suas respectivas permissões.**
```bash
  ls -l
```
---
**p19-b: o comando usado aqui foi o `echo` novamente. No entanto, dessa vez da seguinte maneira `echo "<texto qualquer>" >> <nome do arquivo>`. o uso de `>>` faz com que em vez de sobrescrever o que está no arquivo, seja adicionado ao fim.**
```bash
  echo "some text added." >> restricted.txt
```
---
**p20-b: o comando usado aqui foi o `./<nome do arquivo a executar>`. ao executar esse comando no terminal, ele irá executar o arquivo com o nome especificado.**
```bash
  ./hello_executable
```
---
**p21-b: o comando usado aqui foram dois, primeiro o `chmod <permissão> <nome do arquivo>`. Porque o arquivo do desafio não possuia a permissão para poder executá-lo, foi necessário o uso do chmod para conceder essa permissão e em seguida utilizar o comando 
`./challenge_20`**
```bash
  chmod +x challenge_20 && ./challenge_20
```
---
**p22-b: aqui foi necessário `instalar o gcc` que é o compilador da linguagem C. E em seguida usar o `gcc` para fazer a versão compilada do arquivo `compile_me.c`.**

**1° - instalar o gcc:**
```bash
  sudo apt install gcc
```
**2° - compilar o código com o gcc e executá-lo:**
```bash
    gcc compile_me.c -o compile_me && ./compile_me
```
---
**p23-b: Geralmente a execução de um programa possui três saídas:**

- Saída padrão (stdout): É a saída normal gerada pelo programa.

- Erro padrão (stderr): É onde os erros são enviados.

- padrão (stdin): É usada para enviar dados de entrada para o programa.

**E nesse desafio foi utilizado o comando `./<nome do programa> > <nome do arquivo> 2>&1`
o comando `2>&1` no final, avisa que o arquivo `output.txt` conterá tanto as mensagens de saída quanto as mensagens de erro.**

**Se não fosse usado o comando `2>&1`, dentro do output.txt haveria apenas o primeiro output e não tudo como pedia no desafio.**

```bash
    ./redirect > output.txt 2>&1
```
---
**p24-b: para resolver esse desafio é só executar o comando `date`. Ele irá mostrar na tela a data e hora atual do sistema.**
```bash
    date
```
---
**p25-b: assim como no docker (pra quem conhece) no terminal do linux é possível usar o comando `ps` para conseguir verificar os processos que estão em execução. Pra ser mais exato `ps -e`. Mas existem mais flags que podem ser usadas nesse caso.**
```bash
    ps -e
```
---
**p26-b: o comando usado aqui foi o `nproc`. Ao executá-lo ele informará a quantidade de processadores do seu sistema**
```bash
    nproc
```
---
**p27-b: o comando usado aqui foi o `uname -a`. Ao executá-lo, irá informar detalhes completos do sistema como a versão do Linux, nome do computador, etc.**
```bash
    uname -a
```
---
**p28-b: o comando usado aqui foi o `grep -r "texto que você quer encontrar" <nome do diretorio>`. Com ele você escolhe o texto que está procurando e diz o diretório, ao executá-lo será possível identificar em qual arquivo está contido o texto inserido.**
```bash
    grep -r "You found the needle in the haystack!" bunch_of_files/
```
---
**p29-b: o comando usado aqui foi o `head`. Com ele você pode especificar em qual arquivo você quer consultar e quantas linhas da seguinte forma `head -n <numero de linhas> <nome-exemplo>.csv`**
```bash
    head -n 25 people.csv
```
---
**p30-b: o comando usado aqui foi o `tail`. Com ele você pode especificar em qual arquivo você quer consultar e quantas linhas da seguinte forma `tail -n <numero de linhas> <nome-exemplo>.csv`**
**(segue o mesmo padrao do head)**
```bash
    tail -n 25 people.csv
```
---
**p31-i: o comando usado aqui foi aquele mesmo `diff` usado no desafio 15. Porquê? Ele naturalmente em caso de diferenças entre o conteúdo dos arquivos escolhidos, apenas mostrará o que está diferente. Mas para uma melhor visualização podemos ainda usar o `| grep "[<>]"` ao fim do comando para que ele deixe a visualização mais limpa.**
```bash
    diff greeting1.txt greeting2.txt | grep "[<>]"
```
---
**p32-i: aqui utilizei uma combinação do `sleep` e o `echo`, o sleep para aguardar os 5 segundos do desafio e o echo para printar a string.**
```bash
    echo "Hello" && sleep 5 && echo "world!"
```
---
