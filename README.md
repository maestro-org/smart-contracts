# Maestro Smart Contracts Marketplace
Maestro's Managed-contract API offers developer-friendly endpoints for ready-to-deploy smart contracts. The fully managed service aims to improve developer experience and bootstrap Dapp development on Cardano.

This repository is reponsible for housing all of the smart contracts that are (or will soon be) integrated into Maestro's Managed-contract API. The first step of integration is to add your contract to the marketplace. To do this, follow the steps below!

# Contributing
To add a smart contract to the [Smart Contracts Marketplace](https://www.gomaestro.org/smart-contracts), take the following steps:
1. Create a new directory in `contracts/`, named after the contract (e.g. `linear-vesting`).
2. Add a `meta.json` file in that directory, following [this](contracts/meta_template.json) template.
3. Add the smart contract source code in the same directory or add it as a Git [submodule](https://github.blog/2016-02-01-working-with-submodules/).
4. Open a Pull Request with these changes.
5. Shortly after the PR is merged, the contract will be listed in the marketplace!

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
