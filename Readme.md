<!----- Configurations ---------------------------->
 ## 📌 Anotações - Curso treinamento GitHub FSW - Time : 

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
   
  # Retornar alguma nova mudança feitas no arquivo repo. local
  $ git checkout -- index.html

   # Atualizar branch do repo.local com as atualizaçãoes Repo. Origen.
  $ git pull


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