## Sūrya's Description Report

### Files Description Table


|  File Name  |  SHA-1 Hash  |
|-------------|--------------|
| abstractCaelum.sol | 84b5fbeeaeb752003b745a62353c1379519aa962 |
| BasicToken.sol | 191c87a1d2fd4d25a90dc582c8465c1cb52d6207 |
| CaelumAcceptERC20.sol | 50fd03b8b5111da91fc74b79ad6509f2da4dc9af |
| CaelumFundraise.sol | 2769437edf9b760efbe7549936e473f23b1b6693 |
| CaelumMasternode.sol | 85695ae5efea6c6ef19a337f87554732d16eb1bf |
| CaelumMiner.sol | ea54252324dff57fa4618eecc44f9dd40adebbf5 |
| CaelumVotings.sol | 7ae62c129226e41e3eef0eaf1e6d971ec18a4a97 |
| ERC20Basic.sol | 56b1df898336fbe0792b6742a7d8ec77d4aa64bd |
| ERC20.sol | 81d0c1f4c8e6aa6cd45df30695a1853b3a23ae71 |
| ExtendedMath.sol | ce20d45788d4b026f10e95b11e2b5c9800a19a70 |
| IcaelumVoting.sol | 353ba0200ef9690763a63c5875e41400cb3c214b |
| NewMemberProposal.sol | 96ca6f0d45cdd153be915c6be4a822f15cfa2151 |
| NewTokenProposal.sol | 0b2d84c2543b82122da486d4178e950c700fce16 |
| Ownable.sol | 7e21e1474b0eebb078ddf191df618df2ec762f1c |
| SafeMath.sol | 54cfb2460ff5fe93794214eb99729cda30b965e6 |
| StandardToken.sol | 585492b465ce2fb766534922a62f1e7bc0e2362c |


### Contracts Description Table


|  Contract  |         Type        |       Bases      |                  |                 |
|:----------:|:-------------------:|:----------------:|:----------------:|:---------------:|
|     └      |  **Function Name**  |  **Visibility**  |  **Mutability**  |  **Modifiers**  |
||||||
| **abstractCaelum** | Implementation |  |||
| └ | isMasternodeOwner | Public ❗️ |   | |
| └ | addToWhitelist | Internal 🔒 | 🛑  | |
| └ | addMasternode | Internal 🔒 | 🛑  | |
| └ | deleteMasternode | Internal 🔒 | 🛑  | |
| └ | getLastPerUser | Public ❗️ |   | |
| └ | getMiningReward | Public ❗️ |   | |
||||||
| **BasicToken** | Implementation | ERC20Basic |||
| └ | totalSupply | Public ❗️ |   | |
| └ | transfer | Public ❗️ | 🛑  | |
| └ | balanceOf | Public ❗️ |   | |
||||||
| **CaelumAcceptERC20** | Implementation | abstractCaelum |||
| └ | getMiningReward | Public ❗️ |   | |
| └ | addOwnToken | Public ❗️ | 🛑  | |
| └ | addToWhitelist | Internal 🔒 | 🛑  | |
| └ | isAcceptedToken | Internal 🔒 |   | |
| └ | getAcceptedTokenAmount | Internal 🔒 |   | |
| └ | isValid | Internal 🔒 |   | |
| └ | listAcceptedTokens | Public ❗️ |   | |
| └ | getTokenDetails | Public ❗️ |   | |
| └ | depositCollateral | Public ❗️ | 🛑  | |
| └ | withdrawCollateral | Public ❗️ | 🛑  | |
||||||
| **CaelumFundraise** | Implementation | Ownable, BasicToken, abstractCaelum |||
| └ | \<Fallback\> | Public ❗️ |  💵 | |
| └ | buyMasternode | Public ❗️ |  💵 | |
| └ | receivedFunds | Internal 🔒 | 🛑  | |
||||||
| **CaelumMasternode** | Implementation | Ownable, CaelumFundraise, CaelumVotings, CaelumAcceptERC20 |||
| └ | addGenesis | Public ❗️ | 🛑  | onlyOwner |
| └ | closeGenesis | Public ❗️ | 🛑  | onlyOwner |
| └ | addMasternode | Internal 🔒 | 🛑  | |
| └ | updateMasternode | Internal 🔒 | 🛑  | |
| └ | updateMasternodeAsTeamMember | Internal 🔒 | 🛑  | |
| └ | isTeamMember | Public ❗️ |   | |
| └ | deleteMasternode | Internal 🔒 | 🛑  | |
| └ | isPartOf | Public ❗️ |   | |
| └ | removeFromUserCounter | Internal 🔒 | 🛑  | |
| └ | setMasternodeCandidate | Internal 🔒 | 🛑  | |
| └ | getFollowingCandidate | Internal 🔒 |   | |
| └ | belongsToUser | Public ❗️ |   | |
| └ | isMasternodeOwner | Public ❗️ |   | |
| └ | getLastPerUser | Public ❗️ |   | |
| └ | calculateRewardStructures | Internal 🔒 | 🛑  | |
| └ | setBaseRewards | Internal 🔒 | 🛑  | |
| └ | _arrangeMasternodeFlow | Internal 🔒 | 🛑  | |
| └ | _emergencyLoop | Public ❗️ | 🛑  | onlyOwner |
| └ | masternodeInfo | Public ❗️ |   | |
| └ | contractProgress | Public ❗️ |   | |
||||||
| **CaelumMiner** | Implementation | StandardToken, CaelumMasternode |||
| └ | \<Constructor\> | Public ❗️ | 🛑  | |
| └ | mint | Public ❗️ | 🛑  | |
| └ | _newEpoch | Internal 🔒 | 🛑  | |
| └ | _hash | Internal 🔒 | 🛑  | |
| └ | _reward | Internal 🔒 | 🛑  | |
| └ | _reward_masternode | Internal 🔒 | 🛑  | |
| └ | _adjustDifficulty | Internal 🔒 | 🛑  | |
| └ | getChallengeNumber | Public ❗️ |   | |
| └ | getMiningDifficulty | Public ❗️ |   | |
| └ | getMiningTarget | Public ❗️ |   | |
| └ | getMiningReward | Public ❗️ |   | |
| └ | getMintDigest | Public ❗️ |   | |
| └ | checkMintSolution | Public ❗️ |   | |
||||||
| **CaelumVotings** | Implementation |  |||
| └ | isMasternodeOwner | Public ❗️ |   | |
| └ | addToWhitelist | Internal 🔒 | 🛑  | |
| └ | addMasternode | Internal 🔒 | 🛑  | |
| └ | updateMasternodeAsTeamMember | Internal 🔒 | 🛑  | |
| └ | isTeamMember | Public ❗️ |   | |
| └ | pushProposal | Public ❗️ | 🛑  | |
| └ | handleLastProposal | Internal 🔒 | 🛑  | |
| └ | discardRejectedProposal | Public ❗️ | 🛑  | |
| └ | LastProposalCanDiscard | Public ❗️ |   | |
| └ | getTokenProposalDetails | Public ❗️ |   | |
| └ | pastProposalTimeRules | Public ❗️ |   | |
| └ | becomeVoter | Public ❗️ | 🛑  | |
| └ | voteProposal | Public ❗️ | 🛑  | |
| └ | reachedMajority | Public ❗️ |   | |
| └ | majority | Internal 🔒 |   | |
| └ | reachedMajorityForTeam | Public ❗️ |   | |
| └ | majorityForTeam | Internal 🔒 |   | |
||||||
| **ERC20Basic** | Implementation |  |||
| └ | totalSupply | Public ❗️ |   | |
| └ | balanceOf | Public ❗️ |   | |
| └ | transfer | Public ❗️ | 🛑  | |
||||||
| **ERC20** | Implementation | ERC20Basic |||
| └ | allowance | Public ❗️ |   | |
| └ | transferFrom | Public ❗️ | 🛑  | |
| └ | approve | Public ❗️ | 🛑  | |
||||||
| **ExtendedMath** | Library |  |||
| └ | limitLessThan | Internal 🔒 |   | |
||||||
| **IcaelumVoting** | Interface |  |||
| └ | getTokenProposalDetails | External ❗️ |   | |
| └ | getExpiry | External ❗️ |   | |
| └ | getContractType | External ❗️ |   | |
||||||
| **NewMemberProposal** | Implementation | IcaelumVoting |||
| └ | \<Constructor\> | Public ❗️ | 🛑  | |
| └ | getTokenProposalDetails | Public ❗️ |   | |
| └ | getExpiry | External ❗️ |   | |
| └ | getContractType | External ❗️ |   | |
||||||
| **NewTokenProposal** | Implementation | IcaelumVoting |||
| └ | \<Constructor\> | Public ❗️ | 🛑  | |
| └ | getTokenProposalDetails | Public ❗️ |   | |
| └ | getExpiry | External ❗️ |   | |
| └ | getContractType | External ❗️ |   | |
||||||
| **Ownable** | Implementation |  |||
| └ | \<Constructor\> | Public ❗️ | 🛑  | |
| └ | renounceOwnership | Public ❗️ | 🛑  | onlyOwner |
| └ | transferOwnership | Public ❗️ | 🛑  | onlyOwner |
| └ | _transferOwnership | Internal 🔒 | 🛑  | |
||||||
| **SafeMath** | Library |  |||
| └ | mul | Internal 🔒 |   | |
| └ | div | Internal 🔒 |   | |
| └ | sub | Internal 🔒 |   | |
| └ | add | Internal 🔒 |   | |
| └ | mod | Internal 🔒 |   | |
||||||
| **StandardToken** | Implementation | ERC20, BasicToken |||
| └ | transferFrom | Public ❗️ | 🛑  | |
| └ | approve | Public ❗️ | 🛑  | |
| └ | allowance | Public ❗️ |   | |
| └ | increaseApproval | Public ❗️ | 🛑  | |
| └ | decreaseApproval | Public ❗️ | 🛑  | |


### Legend

|  Symbol  |  Meaning  |
|:--------:|-----------|
|    🛑    | Function can modify state |
|    💵    | Function is payable |
