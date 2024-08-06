# MBA Cloud - exercicio01

Config Inicial 

# Iniciando Repo
git init

# Conectanto no repositório remoto
git remote add origin https://github.com/lebarbos/exercicio01.git

# Realizando Pull do Repositorio
git pull origin main

# Alterando arquivo Readme.md
vi readme.md

# Configurando Nome e email 
git config --global user.name "Leandro Barbosa"
git config --global user.email "lebarbosa@hotmail.com"



# Execução do Exercício.


# A- Criar Arquivo.txt com conteúdo 01. 
echo 01 > arquivo.txt

# B - Adicionar o arquivo no staging e conferir o status

git add . \
git status \

Output \
lebarbos@LCB-PC:git status
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   arquivo.txt

# C - Commitar o arquivo do staging com a descrição "git add example - arquivo.txt"

git commit -m "git add example - arquivo.txt"

