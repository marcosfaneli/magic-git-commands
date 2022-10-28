# adicionar arquivos ao últmo commit
  git commit --amend

# rebase branch
  git checkout dev
  git pull origin dev
  git checkout feature/SGXP-uahca-uahca
  git rebase dev 
  git log
  ## Em caso de conflito, resolver o conflito
    git rebase --continue
  git push origin feature/SGXP-uahca-uahca -f

# Rename a branch
  git branch -m <oldname> <newname>


# Linking to remote repo
 git init
 git add *
 git commit -a -m 'Initial commit'
 git remote add origin git@github.com:username/repo.git 

# Quando foi alterado hash dos commits local, ficando diferente do remoto. atualiza local primeiro e depois sobre as alterações
 git pull origin nome_branch --rebase -f

# Cancelar um merge(pull ou rebase) em andamento
 git reset --hard HEAD

# Sobrepor uma branch
link: http://stackoverflow.com/questions/2763006/change-the-current-branch-to-master-in-git

git checkout outra_branch
git merge --strategy=ours master    # Mantém o conteúdo da branch, porém grava o merge
git checkout master
git merge outra_branch             # Faz o merge de volta para a master 


# Limpar cache de usuários
git config --global --unset credential.helper
