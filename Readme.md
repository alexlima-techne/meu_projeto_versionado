<!----- Configurations ---------------------------->
 ## 📌 Anotações Treinamento Curso GitHub - time FSW  : 

Abaixo deixo a lista de comando executados durante o treinamento: **_GitHub_**, o repositorio onde estou acessando o projeto na conta Git-trabalho, acessar pelo navegador **_https://github.com/alexlima-techne_** 

<br>

##  💻- Lista Comandos Basicos GitHub

```bash
  # Criar a pasta de um  projeto local
  $ mkdir meu_projeto_versionado

  # Iniciar um novo repósitorio local
  $ git init

  # Adicionar arquivo especifico no repositório local
  $ git add index.html

  # Adicionar Todos arquivos no repositório local
  $ git add .

  # Voltar estado de add. do unstage no repositório local
  $ git reset index.html

  # Remover arquivo do Untracked no repositório servidor
  $ git rm index.html

  # Deletar(apagar) o arquivo do repositório local
  $ git rm -f index.html
  
  # consulta o status de staged dos arquivos
  $ git status
  
  # Executar um commit de arquivos
  $ git commit -m "Meu primeiro Commit"

  # Enviar os Commit's do repo. local para repo. Remoto (origem).
  $ git push
   
  # Retornar alguma nova mudança feitas no arquivo repo. local
  $ git checkout -- index.html

  # Atualizar branch do repo.local com as atualizaçãoes Branch Repo. Origen.
  $ git pull
  # Nota: este comando tem as mesmas funções que "git fech" e "git merge".

  # Atualizar o ponteiro branch (origem) com branch (local).
  $ git fetch
  # Nota 1: Quando fizer uma atualização do seu arquivo github-Origem, vai ajustar 
  # a branch local, contudo vale usar o comand. git merge para atualizar arquivos.
  # Nota 2: Serve para informar estado atual das branchs.
   
  # Fazer o merge de arquivo di repo.(origem) para repo.local
  $ git merge 
  # Antes usar o comando fetch, para atualizar posição do ponteiro no branch.

  
  # Consultar históricos de Commits
  $ git log

  # Consulta referencia de Head log commits
  $ git reflog

  # Criar tags repo. local
  $ git tag v.1.1
  # Antes, tem que subir os ultimos commits

  # Subir atualização de tag. para repo.(remoto) Origem
  $ git push --tags

  # Criar Branch através de Repo.local
  $ git branch feature/atualizacao_template 

  # Consultar uma branch local
  $ git branch

  # Deletar ( apagar) branch local
  $ git branch -D feature/atualizacao_template

  # Para acessar uma branch
  $ git checkout feature/update_template

  # fazer Merge de branch local para  branch Master(principal) origin.
  $ git merge feature/update_template
  # Nota: para atualizar Git Remoto Repo. Origin,  execute comando $git push.

```
 

##  ⚙- Configurações GitHub

```bash
  # Para Definir credenciais do ssh user 'store'
  # objetivo: usar estrategia 'store',buscar usuarios e senhas para poder autenticar automativamente.  
  $ git config --global credential.helper 'store'

  
  # Consultar credenciais do usuario e senha salvo local.
  # Este arquivo é oculto e local, não deve compartilhar.
  $ vi .git-credentials

  # Consultar se existe um repository Origen - Nuvem(github)
  $ git remote -v

  # Linkar um repository Origen(gitHub) no repositorio local(gitbash)
  $ git remote add origin https://github.com/alexlima-techne/meu_projeto_versionado.git
  # Nota: Caso tenha configurado mais key ssh. adicionar SSH com nome origem
  # Exemplo: 
  # Ajustar de "git@github.com:alexlima-techne/meu_projeto_versionado.git" 
  # para "git remote add origin git@github.com-trabalho:alexlima-techne/meu_projeto_versionado.git"
 
  # Clonar um repositorio repository Origen(gitHub) para repository local.
  # Dica: https://github.com/git-tips/tips - exemplos comandos github.
  $ git clone https://github.com/git-tips/tips.git
```
#