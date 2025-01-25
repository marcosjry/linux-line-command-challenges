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
**p9-b: o comando pra realizar a tarefa é o `cat <nome do arquivo>.txt > <nome do arquivo>.txt`
ele criará um arquivo vazio com o nome escolhido.**
```bash
 cat empty.txt > empty.txt
```
**p10-b: aqui o comando pra realizar o desafio é o `rm <nome do arquivo>` ele removerá o arquivo que for passado pra ele e em caso de erro, ele avisa o que aconteceu.**
```bash
 rm empty.txt
```

