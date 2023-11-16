# Conditions

## Explication

Une condition vous permet de vérifier l'exactitude de certaines informations, mais aussi de s'assurer de la valeur de vos variables.

## Ecriture

```python
if condition:
    return True # La condition est remplie, nous passons alors dans cette partie
elif autre_condition:
    return False # La première condition n'est pas remplie, on vérifie si la deuxième condition est remplie. Si oui, on passe dans cette partie.
else:
    return None # Aucune des conditions sont remplies, on va alors dans "la branche par défaut"
```

## Types de conditions

Prenons commes variables `bigValue`, `smallValue` et `trueVal` tels que:  
```python
bigValue = 560
smallValue = 15
trueVal = True
```

- `>` Strictement supérieur à -> `if bigValue > smallValue` retournera `True`.  
- `<` Strictement inférieur à -> `if bigValue < smallValue` retournera `False`.
- `>=` Supérieur ou égal à -> `if bigValue >= 560` retournera `True`.
- `<=` Inférieur ou égal à -> `if bigValue <= 559` retournera `False`.
- `==` Egal à -> `if bigValue == 560` retournera `True`. `if bigValue == "560"` retournera également `True`.
- `not` N'est pas -> `if not trueVal` retournera `False`. `if trueVal` retournera `True`.
- `and` Et, multiple conditions -> `if bigValue < smallValue and trueVal` retournera `False`.
- `or` Ou, multiple conditions -> `if bigValue < smallValue or trueVal` retournera `True`.

_Vous pouvez enchaîner plusieurs `and` et `or` dans la même branche. Vous pouvez également utiliser des parenthèses._

## It's your turn

Complétez les fonctions.