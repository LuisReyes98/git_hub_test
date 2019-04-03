Notas:

```git reset --soft [commit]``` , reseta los cambios pero los deja en el working directorie solo hace falta hacer commit 

```git reset --mixed [commit] ``` , resetea los cambios y los quita del working direcorie hay que hacer ```git add``` una vez mas


```
git reset HEAD^
```
retorna el head un commit deshaciendo el ultimo commit 


# GIT SUPERLOG
```
git config --global alias.superlog "log --graph --abbrev-commit --decorate --date=relative --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all"git config --global alias.superlog "log --graph --abbrev-commit --decorate --date=relative --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all"
```