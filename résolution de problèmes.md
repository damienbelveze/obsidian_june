# execute-code

Si Python est installé, le code peut générer une erreur de type "ENOENT". Le plugin va chercher la version de Python installée sur l'ordinateur. Si c'est Python3 qui est installé, il ne va pas le trouver parce qu'aucune équivalence n'est faite entre Python et Python3 (Python3 est par défaut sur les versions récentes de GNU/Linux, il faut le télécharger sur Windows)
Pour créer un alias de Python3 pour Python, suivre les indications suivantes (droits d'admin requis) : 


```shell
sudo ln -s /usr/bin/python2.7 /usr/bin/python2 
sudo ln -s /usr/bin/python2 /usr/bin/python
```

([source](https://askubuntu.com/questions/1144446/python-installed-in-ubuntu-but-python-command-not-found))