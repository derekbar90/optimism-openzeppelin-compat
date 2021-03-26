# optimism-openzeppelin-compat

This repo contains patches needed to use the OpenZeppelin contracts with Optimism L2.

Example: When using Optimism ETH is not supported and instead WETH must be used. When using OpenZeppelin Address contract via ERC20, there are balance checks for ETH and thus the compilation fails. This patches these issues and allows for seamless development.

# Installation

Use the following command to use:
```
npm i --save @thesatoshicompany/optimism-openzeppelin-compat
```

## Have an additional patch which should be included?
Provide a PR and a review will happen to that it can be included.