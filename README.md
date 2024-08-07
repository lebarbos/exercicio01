# MBA Cloud - exercicio01

# Iniciando Repo
git init

# Configurando Nome e email 
git config --global user.name "Leandro Barbosa" -force

git config --global user.email "lebarbosa@hotmail.com" -force


# Execução do Exercício.

# A- Criar Arquivo.txt com conteúdo 01. 
echo 01 > arquivo.txt

# B - Adicionar o arquivo no staging e conferir o status

git add . \
git status 

Output: \
lebarbos@LCB-PC:git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   arquivo.txt

# C - Commitar o arquivo do staging com a descrição "git add example - arquivo.txt"

git commit -m "git add example - arquivo.txt"

Output:
[main (root-commit) b3d2c3c] git add example - arquivo.txt
 1 file changed, 1 insertion(+)
 create mode 100644 arquivo.txt

# D - Sobrescrever o conteúdo do arquivo.txt:
echo 02 > arquivo.txt

# E - Verificar o diffing no arquivo
git diff arquivo.txt
output :
diff --git a/arquivo.txt b/arquivo.txt
index 8a0f05e..9e22bcb 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-01
+02

# F - Adicionar novamente o arquivo no staging e conferir o status
git add arquivo.txt
git status

On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   arquivo.txt

# G - Verificar o diffing no arquivo
 git diff --staged arquivo.txt 

Output:
diff --git a/arquivo.txt b/arquivo.txt
index 8a0f05e..9e22bcb 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-01
+02


# H - Sobrescrever o conteúdo do arquivo.txt:
echo 03 > arquivo.txt

# I - Verificar o diffing no arquivo
git diff arquivo.txt

output: 
diff --git a/arquivo.txt b/arquivo.txt
index 9e22bcb..75016ea 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-02
+03

# J - Fazer o restore do arquivo da área de staging e verificar o status
git restore --staged arquivo.txt
git status 

Output: 
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   arquivo.txt
no changes added to commit (use "git add" and/or "git commit -a")

# K - Realizar o commit do arquivo e verificar o log

git add arquivo.txt
git commit -m "Commit restored from j"

Output:
[main 2fd4a78] Commit restored from j
 1 file changed, 1 insertion(+), 1 deletion(-)

 Git log

commit 2fd4a7822c9cd49b9b781732c42fec39b9b86d7c (HEAD -> main)
Author: Leandro Barbosa <lebarbosa@hotmail.com>
Date:   Wed Aug 7 10:48:34 2024 -0300

    Commit restored from j

commit b3d2c3c99dc24d9144a3ac90326044a44c9f437c
Author: Leandro Barbosa <lebarbosa@hotmail.com>
Date:   Wed Aug 7 10:33:20 2024 -0300

    git add example - arquivo.txt


# L -Adicionar um arquivo gitignore com o seguinte conteúdo
vi .gitignore

cat .gitignore 

Output : 

*.txt


# M - Criar um arquivo novo.txt e verificar o status
echo "conteudo" > novo.txt
git status

Output:
On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore
nothing added to commit but untracked files present (use "git add" to track)
