# The Fuel Toolchain

The full stack of tools designed and built by Fuel Labs for enabling/assisting the Fuel application development experience.

Tooling Overview:

- `fuel-core`: The Fuel VM node client.
- `forc`: The Fuel Orchestrator. Includes Sway compiler, packaging and plugin support.
- `Fuel Indexer`: A standalone binary that can be used to index various components of the blockchain. Check out the docs [here](https://fuellabs.github.io/fuel-indexer/master/the-fuel-indexer.html).

Forc plugins by Fuel Labs:

- `forc-fmt`: The Sway code formatter.
- `forc-lsp`: The Sway Language Server Protocol implementation.
- `forc-explore`: Runs the Fuel block explorer.
- `forc-client`: For deploying and running Sway apps via CLI.
- `forc-wallet`: For initializing a wallet, adding accounts and signing transactions.
- `fuelup`: The Fuel toolchain manager - an easy approach to retrieving all of the above.

For more specific documentation on the toolchain, check out the Sway docs [here](https://fuellabs.github.io/sway/v0.19.2/introduction/sway-toolchain.html).

## Building on Fuel

Developers can get everything they need to start creating Sway applications for the Fuel VM with a single toolchain, blessed by the same teams that create the FuelVM and Sway language.

One common issue developers face when working within the Ethereum ecosystem is how to choose a set of tools to get started. Historically, Ethereum's founders have been particularly focused on the low-level details of the protocol, the EVM and to a lesser extent Solidity, leaving the job of creating accessible, high-level tooling to the community. As a result, many disparate projects have appeared from different 3rd parties that aim to provide these high-level solutions such as truffle, dapptools, hard hat, foundry and many more. It can be difficult for new Ethereum developers to navigate this space and to feel comfortable knowing they're making the right choice in selecting one of these toolchains.

In contrast, Fuel Labs take a curated, "batteries-included"-yet-modular approach to providing tooling. We aim to provide a comprehensive, standardized, canonical set of tools that cover not only the lower levels of the stack (like protocol and VM implementations) but the higher level too (such as package management, editor support, common-use plugins and much more). We aim to do so in a manner that is open, transparent and welcoming of external contributions.

To clarify, the goal is not at all to discourage 3rd parties from extending the fuel ecosystem. Rather, we aim to make the official tool-chain so good as to inspire contributions upstream and to collaborate under one unified developer ecosystem. For those cases where our tooling falls short and additions or extensions are required, we provide an extensible plugin system through `forc`, enabling community creativity in a manner that is easily-shareable and familiar to fellow Fuel devs.

The Sway VS Code plugin is a great example of our vision for a unified developer experience. The plugin interacts with the Sway language server, a forc plugin that communicates directly with the Sway compiler and shares much of its code-base. The plugin also allows for spinning up a Fuel node, displaying its status in real-time and (in the near future) interact with your smart contracts via the type script SDK. A complete solution from entirely within the plugin, from one team with a shared vision.

You can start experimenting with the Fuel toolchain by following the [Fuelup Quickstart Guide](https://fuellabs.github.io/fuelup/master/installation/index.html#quickstart).
