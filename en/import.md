# Importation

You'll notice that we've done some tidying up in our code on the right! You now have tabs at the top of your editor. Click on the tabs to view.

As our code is becoming quite long, we have separated it into multiple files to better manage it. This is how you should handle Solidity projects with a lot of lines of code.

When you have multiple files and you want to import one file into another, Solidity uses the keyword `import`.

```js
import "./someothercontract.sol";

contract newContract is SomeOtherContract {

}
```

We have a file named `someothercontract.sol` in the same directory as this contract (that's what `./` means), and it will be imported by the compiler.

## It's your turn

Now that we have a structure with multiple files, we will need to use `import` to read the contents of the other file:

1. Import `birdfactory.sol` into our new file `birdfeeding.sol`.