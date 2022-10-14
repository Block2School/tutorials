# Smart contract

### Introduction :

---

Les smart contract sont simplement des programmes stockés sur une blockchain qui s'exécutent lorsque des conditions prédéterminées sont remplies. Ils sont généralement utilisés pour automatiser l'exécution d'un accord afin que tous les participants puissent être immédiatement certains du résultat, sans intervention d'un intermédiaire ni perte de temps.

### Tuto 1 : Créer un smart contract

---

Le contract : 

Un contrat ****(contract) permet d'encapsuler du code Solidity, c'est la composante fondamentale de toutes applications Ethereum - toutes les variables et fonctions appartiennent à un contrat, et ce sera le point de départ de tous vos projets.

Voici un exemple de contrat vide : 

 

```solidity
contract MyContract {

}
```

Pragma :

Tout code source en Solidity doit commencer par un "pragma version" - une déclaration de la version du compilateur Solidity que ce code devra utiliser. Cela permet d'éviter d'éventuels problèmes liés aux changements introduits par des futures versions du compilateur.

Cela ressemble à ça : `pragma solidity ^0.4.19;` (la dernière version de Solidity au moment de la rédaction de cet article étant 0.4.19).

Pour résumer, voici un contrat de base - la première chose que vous devez écrire à chaque fois que vous commencerez un nouveau projet :

```solidity
pragma solidity ^0.4.19;

contract MyContract {

}
```

### Tuto 2 : Variables d’état et entiers

---

Les variables d'état sont stockées de manière permanente dans le stockage du contrat. Cela signifie qu'elles sont écrites dans la blockchain Ethereum. C'est comme écrire dans une base de données.

```solidity
contract MyContract {
	uint myUnsignedInteger = 100;
}
```

Dans cet exemple de contrat, nous avons créé un `uint` appelé `myUnsignedInteger`qui a pour valeur 100 et qui sera stocké de manière permanente dans la blockchain.

Le type de données `uint` est un entier non signé, cela veut dire que **sa valeur doit être non négative**. Il existe aussi un type de données `int` pour les entiers signés.

<aside>
⚠️ Remarque: En Solidity, `uint` est en fait un alias pour `uint256`, un entier non signé de 256 bits. Vous pouvez déclarer des uints avec moins de bits - `uint8`, `uint16`, `uint32`, etc. Mais en général il est plus simple d'utiliser `uint` sauf dans des cas spécifiques.

</aside>