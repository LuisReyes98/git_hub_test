# Notas:

#### git reset
reseta los cambios pero los deja en el working directorie solo hace falta hacer commit 
```git reset --soft [commit]``` , 

resetea los cambios y los quita del working direcorie hay que hacer ```git add``` una vez mas
```git reset --mixed [commit] ```  

retorna el head un commit deshaciendo el ultimo commit 
```
git reset HEAD^
```

#### git log
Muestra todos los commit incluso tras un reset hard
```
git log --reflog
```

Muestra el log con diffs
```
git log -p
```
#### GIT SUPERLOG
```
git config --global alias.superlog "log --graph --abbrev-commit --decorate --date=relative --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all"git config --global alias.superlog "log --graph --abbrev-commit --decorate --date=relative --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all"
```

#### Configurar variables de git 
```
git config --global #variable de forma global

git config --local #variable solo en este repositorio
```

#### Configurar vs code como editor
git config --global core.editor "code --wait"

#### Crear ramas
```
git brach [nombre]
```

#### Cambiar nombre de ramas
```
git branch -m responsive RD

```

#### checkout

```
git checkout [branch name | commit]
```

##### merge

teniendo dos ramas debo hacer checkout a la rama que quiero que reciba los datos 
y luego
```
git merge [branch name]
```

git merge [rama]: Nos permite mezclar los cambios realizados en dicha rama con la rama en la que estamos.

fast-forward: los mezcla automáticamente
recursive/auto-merging: ambas ramas salieron al mismo tiempo y hay algo nuevo en la rama que la otra no recuerda, por eso hace la mezcla recursiva.
manual merge: nos va a tocar decirle a git específicamente los cambios que queremos mezclar

#### git rebase
es peligroso y solo deberia aplicarse en local

git rebase: hace prácticamente lo mismo que merge, cambiamos la historia de nuestro proyecto sin crear bifurcaciones del proyecto. Es mejor usar merge
Usar solo git rebase de manera local.
```
git rebase [branch name]
```

-i: de manera interactiva, nos abrira el editor que tengamos definido en la configuración de git.
```
git rebase -i [branch name]
```


#### git cherry-pick

Te permite extraer un unico commit y aplicar sus cambios en la rama actual
```
git cherry-pick [commit hash]
```

## GIT HUB

#### remote 

Añadir primer remoto
```
git remote add origin [ssh/https]
```
ver version 
```
git remote -v
```
eleminar remote
```
git remote remove [name]
```

#### pull y fetch 

traer datos con pull 
```
git pull origin master
```

traer datos con fetch 
```
git fetch origin master 
```
y luego 
```
git merge origin/master
```

