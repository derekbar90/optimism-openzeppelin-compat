
# optimism-openzeppelin-compat
[![NPM Package](https://img.shields.io/npm/v/@thesatoshicompany/optimism-openzeppelin-compat/latest?label=%40thesatoshicompany%2Foptimism-openzeppelin-compat&logo=npm)](https://www.npmjs.com/package/@thesatoshicompany/optimism-openzeppelin-compat)

This repo contains patches needed to use the OpenZeppelin contracts with Optimism L2.

> Example: When using Optimism ETH is not supported and instead WETH
> must be used. When using OpenZeppelin Address contract via ERC20,
> there are balance checks for ETH and thus the compilation fails due to
> an unsupported OPCODE. This patches these issues and allows for
> seamless development.

## Installation

Use the following command to install:

```
npm i --save @thesatoshicompany/optimism-openzeppelin-compat
```

Add the following to the package.json scripts section:

```
"scripts": {
+ "postinstall": "patch-package --patch-dir node_modules/@thesatoshicompany/optimism-openzeppelin-compat/patches"
},
```

`Note: Post install script is needed because this package does not patch files on install automatically. It only provides the appropriate patches and the needed module to apply them.`

`This was a design choice so full control is left to the consumer of the module for if and when they are applied.`

## Supported OpenZeppelin Versions

v3.4.1

## Have an additional patch which should be included?

Provide a PR and a review will happen so that it can be included.