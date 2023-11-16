# Fonctions et typage

## Définition d'une fonction

Une fonction permet d'éxecuter une série d'actions. Elle peut être pratique également lorsque vous avez besoin de répéter plusieurs actions plusieurs fois dans votre code.  

```python
def maFonction(param1, param2): # maFonction est le nom de la fonction, on peut y inclure un ou plusieurs paramètres.
    return param1 > param2 # Retourne le résultat de la condition (True ou False)
```

Une fonction peut retourner une valeur qui peut alors être récupérée par une variable comme ceci:

```python
result = maFonction(3, 5) # result vaudra False.
```

## Typage

Il est possible depuis les versions les plus récentes de Python de typer les variables, les paramètres et les retours de fonctions. Voici comment s'y prendre:

### Fonction

```python
def maFonction(param1: int, param2: int) -> bool: # Ici notre fonction prend deux paramètres de type int et retournera un bool.
    return param1 > param2
```

Le typage n'est pas strict en python, cela veut dire que vous pouvez très bien utiliser une variable en paramètre de fonction de type str et non de type int dans la fonction ci-dessus. Vous pouvez très bien retourner un type int et non un type bool.  
Il est tout de même préférable de typer les fonctions afin de permettre aux développeurs de mieux se repérer dans votre code.  

### Variable

```pythonb
maVariable: int = 10
monTexte: str = "Mon texte"
```

## It's your turn

Ecrivez la fonction `containStr` avec 3 paramètres :  
- Le premier prend une chaine de caractères
- Le deuxième prend une autre chaîne de caractères
- Le troisième prend un nombre entier

Votre fonction doit retourner `True` si le 1er paramètre contient le même nombre de fois le deuxième paramètre que le troisième.  
Exemple:
```python
containStr("Texte d'exemple", "m", 1) # Doit retourner True car il y a bien 1 m dans le premier paramètre.
containStr("Texte d'exemple", "x", 5) # Doit retourner False car il n'y a pas le même nombre de x dans le premier paramètre.
```