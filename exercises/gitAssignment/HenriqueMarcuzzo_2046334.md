# Git Assignment

1. Descreva qual é a saída dos seguintes comandos
    -  `git branch` 
    ```
    feature-foo
    * master
    ```

    -  `git checkout BRANCH_NAME` (USE THE NAME OF AN EXISTING BRANCH)
    ```
    Switched to branch 'feature-foo'
    ```
    -  `git log --decorate`
    ```
    commit a70a8e9d3c5390e367028faf033f2a9ef03d2e91 (HEAD -> feature-foo)
    Author: Igor Steinmacher <igorsteinmacher@gmail.com>
    Date:   Fri Aug 24 15:29:22 2018 -0700

        Adding header of method foo()

    commit 309b0d73ff9c2163591c9e96e307fe61b4c8f58a
    Author: Igor Steinmacher <igorsteinmacher@gmail.com>
    Date:   Fri Aug 24 15:27:16 2018 -0700

        Adding class A skeleton

    commit 9c1eeb8901b0926ce7fa13cc6ce0a1876fc4179b
    Author: Igor Steinmacher <igorsteinmacher@gmail.com>
    Date:   Fri Aug 24 15:26:44 2018 -0700

        Creating all files (all empty)
    ```



2. Tente usar `git log --graph --all`. O que acontece?
```
* commit f67f266cf420735187053f10d32e2c0f7cbc5a43 (master)
| Author: Igor Steinmacher <igorsteinmacher@gmail.com>
| Date:   Fri Aug 24 15:30:05 2018 -0700
| 
|     Adding class B skeleton
|   
| * commit a70a8e9d3c5390e367028faf033f2a9ef03d2e91 (HEAD -> feature-foo)
|/  Author: Igor Steinmacher <igorsteinmacher@gmail.com>
|   Date:   Fri Aug 24 15:29:22 2018 -0700
|   
|       Adding header of method foo()
| 
* commit 309b0d73ff9c2163591c9e96e307fe61b4c8f58a
| Author: Igor Steinmacher <igorsteinmacher@gmail.com>
| Date:   Fri Aug 24 15:27:16 2018 -0700
| 
|     Adding class A skeleton
| 
* commit 9c1eeb8901b0926ce7fa13cc6ce0a1876fc4179b
  Author: Igor Steinmacher <igorsteinmacher@gmail.com>
  Date:   Fri Aug 24 15:26:44 2018 -0700
  
      Creating all files (all empty)
```

3. Use `git diff BRANCH_NAME`  para ver as diferenças de um ramo e do ramo atual.
   Sumarize as diferenças do master e do outro ramo.

   * Diferença da branch ```feature-foo``` para a branch ```master```.

    ```
    diff --git a/A.java b/A.java
    index 3ea227e..674b8ce 100644
    --- a/A.java
    +++ b/A.java
    @@ -1,4 +1,7 @@
    public class A {
    -
    +   
    +   public void foo() {
    +   
    +   }
    
    }
    diff --git a/B.java b/B.java
    index ae64e6b..e69de29 100644
    --- a/B.java
    +++ b/B.java
    @@ -1,4 +0,0 @@
    -public class B {
    -
    -
    -}
    ```

4. Escreva uma sequencia de comandos para mesclar o ramo não-master no `master`

```
$ git add –A
$ git commit
$ git checkout master
$ git merge feature-foo
```


5. Escreva um comando (ou sequência) para (i) criar um novo ramo chamado `math` (do` master`)
e (ii) mudar para este ramo

```
$ git branch math master
```
   
6. Edite B.java adicionando o código abaixo ao conteúdo do arquivo
```java
System.out.println("I know math, look:")
System.out.println(2+2)
```

7. Escreva o comando (ou sequencia) para realizar o commit de suas mudanças
```
$ git add -A
$ git commit -m "I know math"
```

8. Volte para o branch `master` e mude B.java adicionando o seguinte código-fonte (confirme sua mudança para` master`):
```java
System.out.println("Hello World")
```

9. Escreva uma sequência de comando para mesclar o branch `math` em` master` e descreva o que aconteceu
```
$ git merge math
Auto-merging B.java
CONFLICT (content): Merge conflict in B.java
Automatic merge failed; fix conflicts and then commit the result.
```
   
10. Escreva um conjunto de comandos para abortar a mesclagem
```
$ git merge --abort
```
   
11. Agora repita o item 9, mas prossiga com a mesclagem manual (Editando B.java). Todas as funções implementadas são necessárias. Explique o seu procedimento
```
$ git merge --no-commit math
$ nano B.java # Adicionando as alterações de ambas as branch
```

12. Escreva um comando (ou conjunto de comandos) para prosseguir com a mesclagem e atualizar o branch `master`
```
$ git add -A
$ git commit -m "Resolving Conflicts from 'master' and 'math'"
[master 4abcd48] Resolving Conflicts from 'master' and 'math'
```



 
