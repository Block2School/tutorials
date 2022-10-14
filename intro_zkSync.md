# Intro to zkSync

Both Ethereum and zkSync “speak” a language called JSON-RPC that is not human-readable. Luckily, they provide libraries that hide all the complexity below the surface, so you only need to know a bit of JavaScript.

## **Initialize your Node.js project**

Each Node.js project must contain at least one `package.json` file, usually located in the root directory of your project. This file identifies the project and lists the packages your project depends on, making your build reproducible.

You can create a `package.json` file by using a text editor, but the quickest way is to run the `npm init` command and pass it the `-y` flag as follows:

```bash
npm init -y
```

What is the `-y` flag, you ask?

The `-y` flag specifies that you want to accept all the defaults `npm` suggests based on information extracted from the current directory.

## **Install dependencies**

We assume that `npm` and `node` are installed on your computer, and now we want you to install `ethers` and `zksync`.

The syntax for installing a package using `npm` looks like this: