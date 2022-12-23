# rounds

This repository stores all the previous funding rounds ran by [CLR.fund](https://clr.fund). The data in the JSON files are used by the static pages, i.e. leaderboard and project pages, in the CLR.fund app. This allows the CLR.fund app to display previous rounds without accessing the smart contracts or the subgraph.

## Directory structure

/
├─── rounds.json
├─── /xdai
│      └──/0xbC8b6F9e55466217522ce382047191312e51e67D.json
│      └──/0x18604d042A77C6Ed870Bb86Bc59042daf20BC2Fe.json
│      └──/0xb9652b7Cf43b6ec46c8d69728550D91201D609fa.json


- rounds.json: contains a list of all the previous funding rounds
- `roundContractAddress`.json: contains information about the specific funding round. Funding rounds ran on the same network will be stored in the same network folder.


## How to generate the JSON files

All the JSON files are generated using the `fetch-round` task in the CLR.fund [monorepo](https://github.com/clrfund/monorepo) repository. You'll need the etherscan API key to run the task. For example, you can get the etherscan API key from [gnosisscan.io](https://gnosisscan.io).

For example, to generate the previous round for xdai:
```
git clone https://github.com/clrfund/monorepo.git
cd monorepo
yarn && yarn build
cd contracts
yarn hardhat fetch-round --output-dir <output-directory> --network xdai --etherscan-api-key <etherscan-api-key> --round-address 0xbC8b6F9e55466217522ce382047191312e51e67D
```
