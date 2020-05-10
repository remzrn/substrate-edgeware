# Edgeware-specific instructions

This is a modification of the substrate main node to match Edgeware functionalities. To setup the building environment, one can follow the instructions for substrate listed below.
Assuming the build environment is setup, the instructions are

Building  Edgeware alternode:
```
cargo build --release
```
Unfortunately, the runtime has changed so the old configuration formats do not match the new runtime. The chain needs to be generated with hardcoded chain specs
```
./target/release/edgeware-alternode --chain=mainnet-conf --name <INSERT_NAME>
```
At the moment, the chain id is incorrect because of the different configuration hashes. You should see an error about conflicting chain ids.

Below the original readme instructions for substrate:

# Substrate &middot; [![GitHub license](https://img.shields.io/github/license/paritytech/substrate)](LICENSE) [![GitLab Status](https://gitlab.parity.io/parity/substrate/badges/master/pipeline.svg)](https://gitlab.parity.io/parity/substrate/pipelines) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](docs/CONTRIBUTING.adoc)

Substrate is a next-generation framework for blockchain innovation.

## Trying it out

Simply go to [substrate.dev](https://substrate.dev) and follow the [getting started](https://substrate.dev/docs/en/overview/getting-started/) instructions.

## Contributions & Code of Conduct

Please follow the contributions guidelines as outlined in [`docs/CONTRIBUTING.adoc`](docs/CONTRIBUTING.adoc). In all communications and contributions, this project follows the [Contributor Covenant Code of Conduct](docs/CODE_OF_CONDUCT.adoc).

## Security

The security policy and procedures can be found in [`docs/SECURITY.md`](docs/SECURITY.md).

## License

Substrate is [GPL 3.0 licensed](LICENSE).
