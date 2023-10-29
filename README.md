<p align="center">
  <a href="https://www.gomaestro.org/">
    <img src="https://www.gomaestro.org/logos/LandingLogos/DarkLogo.svg" alt="Maestro Logo" width="425" />
  </a>
  <h2 align="center"><a href="https://www.gomaestro.org/">Maestro</a> Smart Contract Marketplace Library</h2>
  <p align="center">
    <a href="https://docs.gomaestro.org/docs/ManagedContracts/Introduction">
      <img src="https://img.shields.io/badge/-Docs-blue?style=flat-square&logo=semantic-scholar&logoColor=white" />
    </a>
    <a href="./LICENSE">
      <img src="https://img.shields.io/github/license/maestro-org/smart-contracts?style=flat-square&label=License" />
    </a>
    <a href="./CONTRIBUTING.md">
      <img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square" />
    </a>
    <a href="https://twitter.com/GoMaestroOrg">
      <img src="https://img.shields.io/badge/-%40GoMaestroOrg-F3F1EF?style=flat-square&logo=twitter&logoColor=1D9BF0" />
    </a>
    <a href="https://discord.gg/ES2rDhBJt3">
      <img src="https://img.shields.io/badge/-Discord-414EEC?style=flat-square&logo=discord&logoColor=white" />
    </a>
  </p>
</p>

# 
Maestro's [Managed Contracts API](https://docs.gomaestro.org/docs/ManagedContracts/Introduction) offers developer-friendly endpoints for ready-to-deploy smart contracts. The fully managed service aims to improve developer experience and bootstrap Dapp development on Cardano.

This repository is reponsible for housing all of the smart contracts that are (or will soon be) integrated into Maestro's Managed-contract API. The first step of integration is to add your contract to the marketplace. To do this, follow the steps below!

# Contributing
To add a smart contract to the [Smart Contracts Marketplace](https://www.gomaestro.org/smart-contracts), take the following steps:
1. Create a new directory in `contracts/`, named after the contract (e.g. `linear-vesting`).
2. Add a `meta.json` file in that directory, following [this](contracts/meta_template.json) template. If you choose to use a logo, you can include it in this directory as well.
3. Add the smart contract source code in the same directory, add it as a Git [submodule](https://github.blog/2016-02-01-working-with-submodules/), or simply paste the public repository URL. NOTE: The smart contract source code must be open sourced to be included in the Marketplace.
4. Open a Pull Request with these changes. Ping [Varderes, Maestro CTO](https://linktr.ee/varderes_maestro) to potentially have it fast tracked!
5. Shortly after the PR is merged, the contract will be available in the Plug-and-Play Marketplace!

### Additional steps for managed contracts
If the the contract you're contributing is managed by Maestro or another provider, feel free to:

6. Contribute a helper [server](https://github.com/maestro-org/smart-contract-servers) to interact with the provider's API endpoints corresponding to the contract.
7. Contribute a user-facing [client](https://github.com/maestro-org/smart-contract-clients) to interact with the contract via the server.

## Smart contract metadata
| Parameter   | Description | Optional (Y/N) | Example     |
| ----------- | ----------- | -------------- | ----------- |
| `name` | Name of the smart contract | N | Linear Vesting |
| `summary` | Short summary of the smart contract | N | Lock tokens with a linear vesting schedule |
| `description` | Detailed descripton of how the smart contract works | Y | Lock tokens with a linear vesting schedule and control the release of tokens over time |
| `documentation` | Link to documentation explaining the | Y | https://docs.gomaestro.org/docs/ManagedContracts/LinearVesting/Introduction |
| `framework` | Smart contract framework used to build the contract | N | Plutarch |
| `royalty` | On-chain cost of using the contract | Y | 1% |
| `author:name` | Name of the smart contract author | N | Anastasia Labs |
| `author:website` | Website of the smart contract | N | https://anastasialabs.com/ |
| `author:logo_64x64` | Public URI the 64x64 logo | Y | https://raw.githubusercontent.com/maestro-org/ispo-metadata/main/maestro-preprod/maestro-logo64x64.png |
| `audit:auditor` | Name of the organization that audiated the smart contract | Y | Anastasia Labs |
| `audit:website` | Website of the auditor | Y | https://anastasialabs.com/ |
| `audit:audit_report` | Public audit report  | N |  |
| `client` | Client side code for interacting with contract | N | https://github.com/maestro-org/smart-contract-clients/linear-vesting |
| `server` | Backend code for interacting with Maestro API endpoints | N | https://github.com/maestro-org/smart-contract-servers/linear-vesting |

# Documentation
* [Complete E2E guide](TBD) on how to fully integrate your contract with the Maestro platform
* [Managed contracts deep dive](https://docs.gomaestro.org/docs/ManagedContracts/Introduction)
* [Maestro Platform](https://docs.gomaestro.org/)
