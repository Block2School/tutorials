# Wallet Metamask

La première chose que nous devons faire dans notre application décentralisé est de nous connecter à notre MetaMask Wallet.

- Nous devons créer une fonction pour voir si l'extension Chrome MetaMask est installée.
- Si MetaMask n'est pas installé nous :
    - Changeons notre connectButton en Click here to install MetaMask (cliquez ici pour installer MetaMask)
    - En cliquant sur ce bouton, nous devrions être dirigés vers une page qui nous permettra d'installer l'extension.
    - Désactiver le bouton
- Si MetaMask est installé, nous :
    - Changeons notre connectButton en Connect
    - En cliquant sur ce bouton, nous devrions pouvoir nous connecter à notre portefeuille MetaMask.
    - Désactiver le bouton

Dans un premier temps, nous devons nous connecter à notre bouton `connectButton` depuis notre index.html

A remplir : 👇

```solidity
const initialize = () => {
  //Basic Actions Section
  const onboardButton = document.getElementById('');
};
```

Réponse : 

```solidity
const initialize = () => {
  //Basic Actions Section
  const onboardButton = document.getElementById('connectButton');
};
```

Ensuite, nous créons une fonction de vérification appelée isMetaMaskInstalled pour voir si l'extension MetaMask est installée.

A remplir : 👇 

```solidity
const initialize = () => {
  //Basic Actions Section
  const onboardButton = document.getElementById('connectutton');

  //Created check function to see if the MetaMask extension is installed
  const isMetaMaskInstalled = () => {
	
	};
};
```

Réponse : 👇

```solidity
const initialize = () => {
  //Basic Actions Section
  const onboardButton = document.getElementById('connectutton');

  //Created check function to see if the MetaMask extension is installed
  const isMetaMaskInstalled = () => {
    //Have to check the ethereum binding on the window object to see if it's installed
    const { ethereum } = window;
    return Boolean(ethereum && ethereum.isMetaMask);
  };
};
```

Ensuite, nous devons créer une fonction `MetaMaskClientCheck` pour voir si nous devons changer le texte du bouton en fonction de l'installation ou non de l'extension MetaMask.

```solidity
const initialize = () => {
  //Basic Actions Section
  const onboardButton = document.getElementById('connectButton');

  //Created check function to see if the MetaMask extension is installed
  const isMetaMaskInstalled = () => {
    //Have to check the ethereum binding on the window object to see if it's installed
    const { ethereum } = window;
    return Boolean(ethereum && ethereum.isMetaMask);
  };

  //------Inserted Code------\\
  const MetaMaskClientCheck = () => {
    //Now we check to see if MetaMask is installed
    if (!isMetaMaskInstalled()) {
      //If it isn't installed we ask the user to click to install it
      onboardButton.innerText = 'Click here to install MetaMask!';
    } else {
      //If it is installed we change our button text
      onboardButton.innerText = 'Connect';
    }
  };
  MetaMaskClientCheck();
  //------/Inserted Code------\\
};
```

### Si MetaMask n’est pas installé :

Dans notre bloc de code où MetaMask n'est pas installé et où nous demandons à l'utilisateur de 'Cliquer ici pour installer MetaMask!', nous devons nous assurer que si notre bouton est cliqué, nous :

- Redirige l'utilisateur vers la page appropriée pour installer l'extension.
- Désactiver le bouton

```solidity
const initialize = () => {
  //Basic Actions Section
  const onboardButton = document.getElementById('connectButton');

  //Created check function to see if the MetaMask extension is installed
  const isMetaMaskInstalled = () => {
    //Have to check the ethereum binding on the window object to see if it's installed
    const { ethereum } = window;
    return Boolean(ethereum && ethereum.isMetaMask);
  };

  //------Inserted Code------\\
  const MetaMaskClientCheck = () => {
    //Now we check to see if MetaMask is installed
    if (!isMetaMaskInstalled()) {
      //If it isn't installed we ask the user to click to install it
      onboardButton.innerText = 'Click here to install MetaMask!';
			//When the button is clicked we call this function
		  onboardButton.onclick = onClickInstall;
		  //The button is now disabled
	    onboardButton.disabled = false;
    } else {
      //If it is installed we change our button text
      onboardButton.innerText = 'Connect';
    }
  };
  MetaMaskClientCheck();
  //------/Inserted Code------\\
};
```

Nous avons créé une fonction qui sera appelée lorsque nous cliquerons sur le bouton et le désactiverons. Penchons nous sur la fonction onClickInstall et créons la logique à l'intérieur de celle-ci.

```solidity
//We create a new MetaMask onboarding object to use in our app
const onboarding = new MetaMaskOnboarding({ forwarderOrigin });

//This will start the onboarding proccess
const onClickInstall = () => {
  onboardButton.innerText = 'Onboarding in progress';
  onboardButton.disabled = true;
  //On this object we have startOnboarding which will start the onboarding process for our end user
  onboarding.startOnboarding();
};
```

Si Metamask est installé :

Ensuite, nous devons revoir notre fonction MetaMaskClientCheck et créer une fonctionnalité similaire à celle que nous avons réalisée dans notre bloc "MetaMask Not Installed" dans notre bloc de code "MetaMask Is Installed".

```jsx
const MetaMaskClientCheck = () => {
  //Now we check to see if Metmask is installed
  if (!isMetaMaskInstalled()) {
    //If it isn't installed we ask the user to click to install it
    onboardButton.innerText = 'Click here to install MetaMask!';
    //When the button is clicked we call th is function
    onboardButton.onclick = onClickInstall;
    //The button is now disabled
    onboardButton.disabled = true;
  } else {
    //If MetaMask is installed we ask the user to connect to their wallet
    onboardButton.innerText = 'Connect';
	  //When the button is clicked we call this function to connect the users MetaMask Wallet
    onboardButton.onclick = onClickConnect;
    //The button is now disabled
    onboardButton.disabled = false;
  }
};
MetaMaskClientCheck();
```

Nous avons maintenant créé une fonction qui sera appelée à chaque fois que nous cliquerons sur le bouton pour déclencher une connexion à notre portefeuille, désactivant ainsi le bouton. Ensuite, nous allons nous plonger dans la fonction onClickConnect et construire la logique dont nous avons besoin à l'intérieur.

Dans cette fonction nous voulons :

- Créer une fonction asynchrone qui va essayer d'appeler la méthode RPC 'eth_requestAccounts'.
- Attraper toutes les erreurs et les enregistrer dans la console.
Sous votre fonction onClickInstall, écrivez/insérez ce code.

```solidity
const onClickConnect = async () => {
  try {
    // Will open the MetaMask UI
    // You should disable this button while the request is pending!
    await ethereum.request({ method: 'eth_requestAccounts' });
  } catch (error) {
    console.error(error);
  }
};
```

## Etherum

Après cela, ce que nous aimerions faire ensuite, c'est que chaque fois que nous appuyons sur le bouton eth_accounts, nous aimerions obtenir notre compte Ethereum et l'afficher. Remplacez le const onboardButton existant en haut de la fonction initialize() par les trois boutons suivants :

```solidity
const getAccountsButton = document.getElementById('getAccounts');
const getAccountsResult = document.getElementById('getAccountsResult');
```

Maintenant que nous avons récupéré notre bouton eth_accounts et notre champ de paragraphe pour l'afficher, nous devons maintenant récupérer les données.

Sous notre fonction MetaMaskClientCheck(), écrivons/insérons le code ci-dessous.

```solidity
//Eth_Accounts-getAccountsButton
getAccountsButton.addEventListener('click', async () => {
  //we use eth_accounts because it returns a list of addresses owned by us.
  const accounts = await ethereum.request({ method: 'eth_accounts' });
  //We take the first address in the array of addresses and display it
  getAccountsResult.innerHTML = accounts[0] || 'Not able to get accounts';
});
```

Si vous vous êtes déjà connecté à votre portefeuille dans la section précédente du tutoriel, vous pouvez aller dans le menu "Sites connectés" de MetaMask et supprimer la connexion localhost. Cela nous permettra de tester à nouveau les deux boutons. Si nous rafraîchissons notre page, et cliquons sur le bouton "ETH_ACCOUNTS", nous devrions voir 'eth_accounts result : Not able to get accounts'.

Allons-y et appuyons à nouveau sur le bouton "Connect", et confirmons l'invite "Connect With MetaMask" et "Connect". Maintenant nous pouvons cliquer à nouveau sur le bouton "ETH_ACCOUNTS" et nous devrions voir l'adresse publique de notre compte MetaMask.

Nous venons de terminer la mise en place de notre fonctionnalité d'actions de base. Vous savez comment vous connecter à MetaMask, voir vos applications connectées et les supprimer, ainsi que récupérer des comptes.