# Notas:

#### reseta los cambios pero los deja en el working directorie solo hace falta hacer commit 
```git reset --soft [commit]``` , 

#### resetea los cambios y los quita del working direcorie hay que hacer ```git add``` una vez mas
```git reset --mixed [commit] ```  

#### retorna el head un commit deshaciendo el ultimo commit 
```
git reset HEAD^
```

#### Muestra todos los commit incluso tras un reset hard
```
git log --reflog
```

#### Configurar variables de git 
```
git config --global #variable de forma global

git config --local #variable solo en este repositorio
```

#### Configurar code como editor
git config --global core.editor "code --wait"

# GIT SUPERLOG
```
git config --global alias.superlog "log --graph --abbrev-commit --decorate --date=relative --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all"git config --global alias.superlog "log --graph --abbrev-commit --decorate --date=relative --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all"
```


#### Crear ramas
```
git brach [nombre]
```

#### Cambiar nombre de ramas
```
git branch -m responsive RD
```