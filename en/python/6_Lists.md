# Listes

Les listes sont des variables particulières. Ces variables ne sont pas instanciées comme pour les dictionnaires que l'on verra plus tard.  
Cela signifie que si l'on crée la liste en dehors d'une fonction, et dans cette fonction, on retire un élément de la liste, même sans retourner la liste, elle sera modifiée.

## Définition

On définit une liste comme ceci:  

```python
myList = [] # Définition de la liste

myList.append("Value") # Ajoute une valeur à la liste
del myList[0] # Supprime l'élément de la liste à l'index 0
len(myList) # Récupère la longueur de la liste
```

## It's your turn

Complétez les fonctions.