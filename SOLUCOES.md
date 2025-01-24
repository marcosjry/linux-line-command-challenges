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
***p5-b: O primeiro comando que me veio a cabeça foi `mkdir foo && cd foo mkdir bar && cd bar && mkdir 1 && cd 1 && mkdir 2 && cd 2 && mkdir 3` mas pela lógica, ele pareceu um pouco confuso apesar de funcional. Então, pesquisei e existe uma forma muito mais simples e ainda diminui as chances de erro. Além disso, aparentemente é necessário a flag `-p`.**
```bash
  mkdir -p foo/bar/1/2/3    
```