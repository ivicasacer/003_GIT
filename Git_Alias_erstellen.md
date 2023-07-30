# Alias in Git erstellen
## _Alias Permanent hinzufügen_






1. Git Bash _Als Administrator_ ausführen

2. Command eingeben:
```ssh
 git config --global --edit
```

3. Automatisch wird deine config Datei in Editor o.ä. ausgeführt.
4. Im Editor unter [Alias] werden deine kürzel eingegeben:
 z.B.:
```ssh
[Alias]

co = Checkout
ci = commit
st = status
```
5. Nach dem dein Alias eingetragen wurde, muss die Datei gespeichert werden um Alias im Bash zu übernehmen.

## _Alias Temporary hinzufügen_

1. Git Bash _als Administrator_ ausführen
2. Den Befehl "Alias "kürzel"="ganzer Befehl"" z.B.
```ssh
alias gp='git pull'
```
#### Dein Alias wird nach dem neustart vom Bash gelöscht!










