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

