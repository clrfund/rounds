# rounds

This repository stores all the previous funding rounds ran by [CLR.fund](https://clr.fund). The data in the json files are used by the static pages, i.e. leaderboard and project pages, in the CLR.fund app. This allows the CLR.fund app to display previous rounds' information without accessing the smart contracts or the subgraph.

## Directory structure

/
├─── rounds.json
├─── /xdai
│      └──/0xbC8b6F9e55466217522ce382047191312e51e67D.json
│      └──/0x18604d042A77C6Ed870Bb86Bc59042daf20BC2Fe.json
│      └──/0xb9652b7Cf43b6ec46c8d69728550D91201D609fa.json


- rounds.json: contains a list of all the previous funding rounds
- `roundContractAddress`.json: contains information about the specific funding round. Funding rounds ran on the same network will be stored in the same network folder.
