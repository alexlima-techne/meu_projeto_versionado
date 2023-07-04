<!----- Configurations ---------------------------->
 ## 📌 Anotações Treinamento Curso GitHub - time FSW  : 

Abaixo deixo a lista de comando executados durante o treinamento: **_GitHub_**, o repositorio onde estou acessando o projeto na conta Git-trabalho, acessar pelo navegador **_https://github.com/alexlima-techne_** 

<br>

##  💻- Lista Comandos Git-Bash

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
  # Nota: caso for primeiro commit, pode usar $ git push -u origin master - u - apelido.
   
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

  # Renomear uma branch local
  $ git branch -m main
  # Nota: antes de fazer o git push. deve atualizar a branche no repo.Remoto, use "$ git push --set-upstream origin main"

  # Deletar ( apagar) branch local
  $ git branch -D feature/atualizacao_template

  # Para acessar uma branch
  $ git checkout feature/update_template

  # fazer Merge de branch local para  branch Master(principal) origin.
  $ git merge feature/update_template
  # Nota: para atualizar Git Remoto Repo. Origin,  execute comando $git push.

  # Criar nova branch, copia base de outra branch - local.
  $ git checkout -b feature/nova_branch
  # Nota: utilizado no momento que faz o merge(master) e pega estado branch atual mais recente.

  # Fazer Atualização Branch(master-Principal), quando teve commits de outras branches
  $ git rebase master 
  # Nota: Após é necessario fazer o "$ git checkout master", em sequida "$ git pull", vai atualizar os arquivo da origem para o repo. local.
  # Dica: Utilizado quando teve alteração de mesmo arquivo em outra branch, contudo a sua,
  # ficou desatualizado e pode ocorrer conflito ao fazer o merge na branch(master).

  # Fazer correção Rebase
  $ git rebase --continue
  # Nota: Antes, faça a correção do arquivo, em seguida "$ git add.", execute novamente o rebase.
  # [ i ] - para texto commit, [ ESC ] - sair modo edição, [ :x ] Salvar commit.
  # Apos  pode fazer "$ git push", para atualizar de branch local comits de sua branch na origin sem haver conflitos.
  
  # Solucionar problemas Push, quando não encontra Branch- Origin Repo.Remoto.
  $ git push --set-upstream origin feature/branchA
  # Nota 01: Este cenario ocorre pois a  branchA, foi criada local, e não existia atualizada na Repo.origin.
  # Nota 02: A branchB, foi criada na Repo.origin e não existia no Repo.local, contudo feito o rebase pegou atualizações da mesma e aplicados na atual branchA.

  # Escolho um determinado commit especifico, e trago para meu repo.local
  $ git cherry-pick feature/mudancas e70da842ece081cda02e3d679fad15374a364080
  # Nota: deve informar a branch e o codigo key commit, que esta no repo.origin(remoto).

  # Voltar commits, para um ponto especifico na branch
  $ git reset 71d13481d768b66148bd1354e04440ed4a96bc12
  # Nota: Atenção pois este comando ira excluir arquivos novos da sua branch,a partir de uma codigo key rash do comite escolhido.
  # Obs: Arquivos alterados retorna para staged para commit, podendo ajustalos ou commitar novamente
  # caso quiser limpar tudo usar "$ git checkout -- ."

  # Para Limpar todos arquivos que deseja eliminar,  alterações de arquivos na branch local
  $ git checkout -- . 

  # Para limpar arquivos de branch, deletar mesmo que permaneção algum difenentes
  $ git clean -f
  # Nota: Atenção - apaga arquivos na branch, não tem opção de restaurar.

  # Para atualizar Push - Force, atualizar mesmo quano commits, estão atras da sua branch local
  $ git push -f
  # Nota: Atualizo a branch local, mesmo que esteja com commits atraz da branch (master-principal).

  # Para apagar os commits e historico dos ultimos 2 commits
  $ git reset HEAD~2
  # Nota: Head~2 - apago os 2 ultimos commits, mantendo o anterior.
 
  # Guardar um Estado de copia do arquivo, para commitar depois
  $ git stash
  # Nota 01: Ser for arquivo novo, é necessario antes adicionar arquivo, então usar $ git Add .
  # Nota 02: Funciona como uma pilha de salvamento então segue seguencia.
  # Dica: usando para quando quer manter um estado de alteração do arquivo caso precisar retornar depois ao ponto de alteração.

  # Para consultar lista de Stash, guardados
  $ git stash list

  # Para voltar alteração o ultim stash da pilha de salvamento
  $ git stash pop

```
 
##  💻 - Lista Comandos e Config. Git-Flow

```bash
  # para consultar os comandos Git Flow
  $ git flow
  # Nota: não é possivel usar este comandos sem antes inicializar o repo. git flow.

  # Iniciar e configurar um novo repósitorio local
  $ git flow init
  # Nota: Para inicia pode escolher a branch [ master-principal]
  # em seguida informar qual proximo name (branch) para relese de versão, caso não tiver 
  # é preciso criar uma nova branch, para isso use:"$ git checkout -b develop", neste caso sera uma feature.
  # 1 criado a nova branch 'develop', dentro dela inicie o comando 'git flow init' que vai sugerir a mesma.
  # 2 seram informado padrões de crição :"feature/ bugfiz/ realese/ hotfix/ support" como modelo é só avançar com enter.
  
  ---------------------------------------------------------------------------
  # Iniciar e criar uma nova branch 
  $ git flow feature start nomebranch
  # Nota 01: Cria uma banch exemplo: ('$ git checkou -b'), baseada na branch DEVELOP.
  # Nota 02: Automaticamente renomeia com feature/nomebranch
  # Nota 03: Passa a usar a nova branch '($ git checkout feature/nomebranch)'

  # Finalizar e faz merge branch 
  $ git flow feature finish nomebranch
  # Nota 01: Merge a feature branch: 'nomebranch' dentro da branch DEVELOP, exemplo:('$ git checkout develop') e ('$ git merge nomebranch').
  # Nota 02: Deleta a feature branch ($ git branch - D feature/nomebranch).
  # Nota 03: Muda para a develop ('$ git checkout develop').

  # Atualizar e publicar  branch Repo. Origin (Remoto)
  $ git flow feature publish nomebranch
  # Nota 01: Criar uma branch remota, exemplo:('$ git push --set-upstream origin feature/nomebranch').

  ---------------------------------------------------------------------------
  # Criar uma Release
  $ git flow release start nomebranch
  #  # Nota 01: Cria uma banch exemplo: ('$ git checkou -b'), baseada na branch DEVELOP.
  # Nota 02: Automaticamente renomeia com release/nomebranch
  # Nota 03: Passa a usar a nova branch '($ git checkout release/nomebranch)'

   # Finalizar Uma branch release
  $ git flow release finish nomebranch
  # Nota 01: Merge a Release branch: 'nomebranch' dentro da branch MASTER, exemplo:('$ git checkout master') e ('$ git merge nomebranch').
  # Nota 02: Cria uma tag com o nome realse/nomebranch ($ git tag release/nomebranch)
  # nota 03: Merge a Release/nomebranch dentro da branch DEVELOP ($ git checkout develop) e ($git merge release/nomebranch)
  # Nota 04: Deleta a realse branch ($ git branch - D release/nomebranch).
  # Nota 05: Muda para a develop ('$ git checkout develop').

  # Atualizar e publicar  branch Release Repo. Origin (Remoto)
  $ git flow release publish nomebranch
  # Nota 01: Criar uma branch remota, exemplo:('$ git push --set-upstream origin release/nomebranch').
  
  -----------------------------------------------------------------------------
   # Criar uma rotiFix
  $ git flow hotfix start nomebranch
  #  # Nota 01: Cria uma banch exemplo: ('$ git checkou -b'), baseada na branch MASTER.
  # Nota 02: Automaticamente renomeia com hotfix/nomebranch
  # Nota 03: Passa a usar a nova branch '($ git checkout hotfix/nomebranch)'

   # Finalizar Uma branch release
  $ git flow hotfix finish nomebranch
  # Nota 01: Merge a Release branch: 'nomebranch' dentro da branch MASTER, exemplo:('$ git checkout master') e ('$ git merge nomebranch').
  # Nota 02: Cria uma tag com o nome hotfix/nomebranch ($ git tag hotfix/nomebranch)
  # nota 03: Merge a hotfix/nomebranch dentro da branch MASTER ($ git checkout develop) e ($git merge hotfix/nomebranch)
  # Nota 04: Deleta a hotfix branch ($ git branch - D hotfix/nomebranch).
  # Nota 05: Muda para a develop ('$ git checkout develop').

  # Atualizar e publicar  branch Release Repo. Origin (Remoto)
  $ git flow hotfix publish nomebranch
  # Nota 01: Criar uma branch remota, exemplo:('$ git push --set-upstream origin release/nomebranch').

 


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
 
  # Atualizar o link de um repositorio Origen(gitHub) no repositorio local(gitbash)
  $ git remote set-url origin git@github.com:alexlima-techne/meu_projeto_versionado.git
  # Nota: neste caso atualizei o endereço do link Url:
  # De    [HTTPS] (Use Git or checkout with SVN using the web URL). 
  # para  [SSH ]  (Use a password-protected SSH key)..

  # Clonar um repositorio repository Origen(gitHub) para repository local.
  # Dica: https://github.com/git-tips/tips - exemplos comandos github.
  $ git clone https://github.com/git-tips/tips.git

  # Consultar config. usuarios perfil Alias.
  $ vi ~/.bashrc

```
#